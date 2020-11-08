---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016187"
---
# <span data-ttu-id="d26ed-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d26ed-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="d26ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d26ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d26ed-103">Virtuális hálózatban VPN-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d26ed-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="d26ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d26ed-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d26ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d26ed-105">DESCRIPTION</span></span>
<span data-ttu-id="d26ed-106">A **New-AzureVNetGateway** parancsmag virtuális MAGÁNHÁLÓZAT (VPN) átjárót hoz létre virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="d26ed-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="d26ed-107">Az átjáró SKU-ának alapértelmezett, normál vagy HighPerformance is megadható.</span><span class="sxs-lookup"><span data-stu-id="d26ed-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="d26ed-108">Megadhatja, hogy milyen típusú, vagy StaticRouting vagy DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="d26ed-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="d26ed-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d26ed-109">EXAMPLES</span></span>

### <span data-ttu-id="d26ed-110">Példa 1: virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="d26ed-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="d26ed-111">Ez a parancs virtuális hálózati átjárót hoz létre a ContosoVN07 nevű virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="d26ed-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="d26ed-112">Az átjáró az alapértelmezett SKU, és dinamikus művelettervet használ.</span><span class="sxs-lookup"><span data-stu-id="d26ed-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="d26ed-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d26ed-113">PARAMETERS</span></span>

### <span data-ttu-id="d26ed-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="d26ed-114">-GatewaySKU</span></span>
<span data-ttu-id="d26ed-115">Annak a virtuális hálózati átjárónak az SKU-számát adja meg, amelyre a parancsmag létrehozta.</span><span class="sxs-lookup"><span data-stu-id="d26ed-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="d26ed-116">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d26ed-116">Valid values are:</span></span> 

- <span data-ttu-id="d26ed-117">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="d26ed-117">Default</span></span> 
- <span data-ttu-id="d26ed-118">Standard</span><span class="sxs-lookup"><span data-stu-id="d26ed-118">Standard</span></span> 
- <span data-ttu-id="d26ed-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="d26ed-119">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26ed-120">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="d26ed-120">-GatewayType</span></span>
<span data-ttu-id="d26ed-121">A parancsmag által létrehozott átjáró típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d26ed-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="d26ed-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d26ed-122">Valid values are:</span></span> 

- <span data-ttu-id="d26ed-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="d26ed-123">StaticRouting</span></span> 
- <span data-ttu-id="d26ed-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="d26ed-124">DynamicRouting</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26ed-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d26ed-125">-Profile</span></span>
<span data-ttu-id="d26ed-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d26ed-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d26ed-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d26ed-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d26ed-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d26ed-128">-VNetName</span></span>
<span data-ttu-id="d26ed-129">Annak a virtuális hálózatnak a megadása, amelyben ez a parancsmag virtuális hálózati átjárót ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="d26ed-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26ed-130">CommonParameters</span></span>
<span data-ttu-id="d26ed-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d26ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26ed-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d26ed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26ed-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26ed-133">INPUTS</span></span>

## <span data-ttu-id="d26ed-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26ed-134">OUTPUTS</span></span>

## <span data-ttu-id="d26ed-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d26ed-135">NOTES</span></span>

## <span data-ttu-id="d26ed-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d26ed-136">RELATED LINKS</span></span>

[<span data-ttu-id="d26ed-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d26ed-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="d26ed-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d26ed-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="d26ed-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d26ed-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="d26ed-140">Átméretezés-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d26ed-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="d26ed-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d26ed-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


