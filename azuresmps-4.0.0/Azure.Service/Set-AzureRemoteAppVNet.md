---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016052"
---
# <span data-ttu-id="54fa6-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="54fa6-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="54fa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="54fa6-103">Egy Azure RemoteApp virtuális hálózat tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="54fa6-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="54fa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54fa6-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54fa6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54fa6-105">DESCRIPTION</span></span>
<span data-ttu-id="54fa6-106">A **set-AzureRemoteAppVNet** parancsmag az Azure RemoteApp virtuális hálózat tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="54fa6-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="54fa6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54fa6-107">EXAMPLES</span></span>

### <span data-ttu-id="54fa6-108">Példa 1: virtuális hálózat tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="54fa6-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="54fa6-109">Ez a parancs a ContosoVNet nevű virtuális hálózat tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="54fa6-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="54fa6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54fa6-110">PARAMETERS</span></span>

### <span data-ttu-id="54fa6-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="54fa6-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="54fa6-112">A DNS-kiszolgálók IPv4-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54fa6-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa6-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="54fa6-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="54fa6-114">A helyi hálózati címtartomány megadása Inter-Domain műveletterv (CIDR) osztályában.</span><span class="sxs-lookup"><span data-stu-id="54fa6-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="54fa6-115">Ennek a virtuális hálózati címtartomány nem lehet átfedésben.</span><span class="sxs-lookup"><span data-stu-id="54fa6-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa6-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="54fa6-116">-Profile</span></span>
<span data-ttu-id="54fa6-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="54fa6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54fa6-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="54fa6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fa6-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="54fa6-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="54fa6-120">A virtuális hálózati címtartomány meghatározása a CIDR jelölésével.</span><span class="sxs-lookup"><span data-stu-id="54fa6-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="54fa6-121">Ennek a magánhálózati IP-címtartományból kell lennie, és nem fedi át a helyi hálózati címet.</span><span class="sxs-lookup"><span data-stu-id="54fa6-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa6-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="54fa6-122">-VNetName</span></span>
<span data-ttu-id="54fa6-123">Az Azure RemoteApp virtuális hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54fa6-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa6-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="54fa6-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="54fa6-125">A virtuális magánhálózat (VPN) eszköz címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54fa6-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="54fa6-126">Ennek csak nyilvános címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="54fa6-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fa6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fa6-127">CommonParameters</span></span>
<span data-ttu-id="54fa6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54fa6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fa6-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fa6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fa6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54fa6-130">INPUTS</span></span>

## <span data-ttu-id="54fa6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54fa6-131">OUTPUTS</span></span>

## <span data-ttu-id="54fa6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54fa6-132">NOTES</span></span>

## <span data-ttu-id="54fa6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54fa6-133">RELATED LINKS</span></span>

[<span data-ttu-id="54fa6-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="54fa6-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


