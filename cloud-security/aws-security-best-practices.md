# AWS Security Best Practices

RedLock or CloudCheckr, GuardDuty on. ASAP.

[https://github.com/toniblyx/prowler](https://github.com/toniblyx/prowler)

[https://github.com/nccgroup/Scout2](https://github.com/nccgroup/Scout2)

I often use scout as a first run at profiling an account when making justifications for spending more time looking at it. It has an HTML based report that is decent enough at showing to folks to get traction.

Prowler is nice because it's command line based and you can just just to run a subset of checks if you're trying to nail something down.

So I ended up creating a lambda that analysis all my cloudtrail logs and alerts me when an unknown ip is found.

System Manager might also be able to help with some things too \(not super familiar with it, but potentially help with patching etc\).

 Use [VPC endpoints](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html) if you only use services that have endpoints and turn off internet access/egress altogether where you can.

Watch out for those costs though; dozens of established endpoints can get expensive fast, especially across multiple VPCs/subnets.

You can find the CIS checks here: [https://github.com/awslabs/aws-security-benchmark/tree/master/aws\_cis\_foundation\_framework](https://github.com/awslabs/aws-security-benchmark/tree/master/aws_cis_foundation_framework)

Suggest you put in a security compliance tool like "Cloud Conformity" which will pretty much cover off most of these and about 1000 other good security practices.Suggest you put in a security compliance tool like "Cloud Conformity" which will pretty much cover off most of these and about 1000 other good security practices.

It will basically do your job for you monitoring your environment and telling you when bad things are deployed or setup.

One other nice thing to do is restrict outbound internet access \(egress\) from your vpc, unfortunately NAT gateways just let everything out. You can do this but using your own transparent proxies for outbound internet using squid. In squid you can basically restrict internet traffic to domains or IPs you whitelist..

Fundamentally for someone to hack into your servers remotely they are gonna want to get a reverse shell and they'll need outbound internet to a dodgy IP origin for that. \(Outside of the obvious OWASP web attack methods, sqli/xss etc\)

AWS' Config team has a list of compliance monitoring rules:

[https://github.com/awslabs/aws-config-engine-for-compliance-as-code](https://github.com/awslabs/aws-config-engine-for-compliance-as-code)

{% embed url="https://github.com/awslabs/aws-config-rules/tree/master/python" %}



{% embed url="https://aws-de-media.s3.amazonaws.com/images/Produktblaetter/AWS-Security-Check-List\_eng.pdf" %}



{% embed url="https://d1.awsstatic.com/whitepapers/architecture/AWS-Security-Pillar.pdf" %}



{% embed url="https://d1.awsstatic.com/whitepapers/compliance/AWS\_CIS\_Foundations\_Benchmark.pdf" %}





