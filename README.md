# Rufus::Scheduler::Win32::Service

A simple wrapper around the rufus-cheduler (https://github.com/jmettraux/rufus-scheduler) to run it as a Windows Service (https://github.com/djberg96/win32-service).

## Installation

Add this line to your application's Gemfile:

    gem 'rufus-scheduler-win32-service'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install rufus-scheduler-win32-service

## Usage

You want to run your rufus-scheduler tasks as a Windows service. This gem provides the boilerplate:

```
require 'rufus/scheduler/win32/service'

class MyService < Rufus::Scheduler::Win32::Service
  def service_init
    # Set up everything and create your scheduled tasks here
    scheduler.every '5m' do |_job|
      logger.info 'Reports of my death have been greatly exaggerated'
    end
  end
end
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
