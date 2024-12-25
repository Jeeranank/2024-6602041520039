 $headers = @{
    "Content-Type" = "application/json"
    "Authorization" = "Bearer 6dfbd2a0da0aacb7073759877c2af8dfa3c414ecbe20589b0418b21a5b24b381b197b9d72c6332863517f4bcfa00421f9b1a8907080dc4fa25174ebb07caa0ebced31a55ed9916c8e93cc728d7fbce6e37cb64a0ab0eb9bc69e0201108b804e8f3a19706c6f5f1995ce37ddaf1fd2a68a48b127ea1813781fc886ca08f71edde"
}

$body = @{
    username = "Jeeranan22"
    email = "ppp2143@hotmail.com"
    password = "P@2511"
} | ConvertTo-Json -Depth 10

Invoke-RestMethod -Uri "http://localhost:8080/api/auth/local/register" -Method POST -Headers $headers -Body $body
