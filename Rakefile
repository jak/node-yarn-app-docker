require 'erb'

task :generate do
    versions = [4,6,7]
    versions.each do |v|
		build_opts = OpenStruct.new(version: v)
  		dockerfile = ERB.new(File.read("./Dockerfile.erb"))
               .result(build_opts.instance_eval { binding })
		File.open("#{v}/Dockerfile", 'w') do |file|
			file.write dockerfile
		end
	end
end

