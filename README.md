# NAME

Amazon::S3::SignedURLGenerator - Amazon S3 Signed URL Generator

# SYNOPSIS

    use Amazon::S3::SignedURLGenerator;

    my $generator = Amazon::S3::SignedURLGenerator->new(
        aws_access_key_id     => $aws_access_key_id,
        aws_secret_access_key => $aws_secret_access_key,
        prefix => 'https://mybucket.s3.amazonaws.com',
        expires => 600, # 10 minutes
    );

    my $url = $generator->generate_url('GET', 'path/file.txt', {});

# DESCRIPTION

Amazon::S3::SignedURLGenerator is just a copy of [Muck::FS::S3::QueryStringAuthGenerator](https://metacpan.org/pod/Muck::FS::S3::QueryStringAuthGenerator) without unnecessary dependencies.

# SEE ALSO

[https://github.com/rbrigham/s3-signed-url](https://github.com/rbrigham/s3-signed-url)

[Muck](https://metacpan.org/pod/Muck)

# AUTHOR

Fayland Lam <fayland@gmail.com>

# COPYRIGHT

Copyright 2017- Fayland Lam

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.
