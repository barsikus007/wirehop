# WireHop(e)

WireHop is a multihop ready WireGuard-in-docker system. You can use wirehop with PBR (not done yet)
WireHop(e) (sane fork of WireHole) is a combination of wg-easy, Pi-hole, and unbound in a compose project with the intent of enabling users to quickly and easily create and deploy a personally managed full or split-tunnel WireGuard VPN with ad blocking capabilities (via Pihole), and DNS caching with additional privacy options (via unbound)

## Install

1. `git clone https://github.com/barsikus007/wirehop.git && cd wirehop`
2. Copy `.env.example` files to `.env` and edit
3. `docker compose up -d --build`

### Firewall tip (ufw)

- `sudo ufw status numbered`
- `sudo ufw allow 12345`
  - `sudo ufw allow 51820/udp`
  - `sudo ufw allow 51821/tcp`
  - `sudo ufw delete NUM`
  - `sudo ufw allow http`
  - `sudo ufw allow https`
- `sudo ufw reload`
