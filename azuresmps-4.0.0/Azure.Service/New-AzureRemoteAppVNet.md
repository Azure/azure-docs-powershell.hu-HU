---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015994"
---
# <span data-ttu-id="ec8f9-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ec8f9-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="ec8f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec8f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8f9-103">Azure RemoteApp virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="ec8f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec8f9-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec8f9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec8f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8f9-106">A **New-AzureRemoteAppVNet** parancsmag létrehoz egy Azure RemoteApp virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="ec8f9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec8f9-107">EXAMPLES</span></span>

### <span data-ttu-id="ec8f9-108">Példa 1: virtuális hálózat létrehozása</span><span class="sxs-lookup"><span data-stu-id="ec8f9-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="ec8f9-109">Ez a parancs létrehoz egy ContosoVNet nevű virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="ec8f9-110">A művelet állapotának meghatározásához használja a **Get-AzureRemoteAppOperationResult** parancsmagot annak a NYOMKÖVETÉSi azonosítónak a megadásával, amelyet a parancsmag ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="ec8f9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec8f9-111">PARAMETERS</span></span>

### <span data-ttu-id="ec8f9-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="ec8f9-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="ec8f9-113">A DNS-kiszolgálók IPv4-címeinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f9-114">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="ec8f9-114">-GatewayType</span></span>
<span data-ttu-id="ec8f9-115">A használni kívánt átjáró típusának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="ec8f9-116">A paraméter elfogadható értékei a következők: StaticRouting vagy DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f9-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="ec8f9-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="ec8f9-118">Olyan karakterláncokat ad meg, amelyek megadják a helyi hálózati címtartomány, az osztály nélküli többtartományos útválasztási (CIDR) jelölést.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="ec8f9-119">Ez a Címterület nem fedi át a virtuális hálózati címterület által az *VirtualNetworkAddressSpace* paraméter által megadott helyet.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f9-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="ec8f9-120">-Location</span></span>
<span data-ttu-id="ec8f9-121">A virtuális hálózat létrehozásának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f9-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec8f9-122">-Profile</span></span>
<span data-ttu-id="ec8f9-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec8f9-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec8f9-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="ec8f9-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="ec8f9-126">Olyan karakterláncot ad meg, amely megadja a virtuális hálózati címterület CIDR jelölését.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="ec8f9-127">Ennek a magánhálózati IP-címtartomány-tartománynak kell lennie, és nem lehet átfedésben a *LocalNetworkAddressSpace* paraméter által megadott helyi hálózati címterület segítségével.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f9-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ec8f9-128">-VNetName</span></span>
<span data-ttu-id="ec8f9-129">Az Azure RemoteApp virtuális hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="ec8f9-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="ec8f9-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="ec8f9-131">A virtuális magánhálózat (VPN) eszköz címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="ec8f9-132">Ennek csak nyilvános címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ec8f9-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="ec8f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8f9-133">CommonParameters</span></span>
<span data-ttu-id="ec8f9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec8f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8f9-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec8f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8f9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec8f9-136">INPUTS</span></span>

## <span data-ttu-id="ec8f9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec8f9-137">OUTPUTS</span></span>

## <span data-ttu-id="ec8f9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec8f9-138">NOTES</span></span>

## <span data-ttu-id="ec8f9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec8f9-139">RELATED LINKS</span></span>

[<span data-ttu-id="ec8f9-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="ec8f9-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="ec8f9-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ec8f9-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="ec8f9-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ec8f9-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="ec8f9-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="ec8f9-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


