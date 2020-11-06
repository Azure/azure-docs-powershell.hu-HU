---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495083"
---
# <span data-ttu-id="4946c-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4946c-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="4946c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4946c-102">SYNOPSIS</span></span>
<span data-ttu-id="4946c-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="4946c-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4946c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4946c-104">SYNTAX</span></span>

### <span data-ttu-id="4946c-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4946c-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4946c-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="4946c-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4946c-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="4946c-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4946c-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="4946c-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4946c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4946c-109">DESCRIPTION</span></span>
<span data-ttu-id="4946c-110">A **Get-AzureRmPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="4946c-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="4946c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4946c-111">EXAMPLES</span></span>

### <span data-ttu-id="4946c-112">1: nyilvános IP-erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="4946c-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="4946c-113">Ez a parancs olyan nyilvános IP-cím típusú erőforrást kap, amelyben a név $publicIPName szerepel az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="4946c-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="4946c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4946c-114">PARAMETERS</span></span>

### <span data-ttu-id="4946c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4946c-115">-DefaultProfile</span></span>
<span data-ttu-id="4946c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4946c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4946c-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4946c-118">-IpConfigurationName</span></span>
<span data-ttu-id="4946c-119">Hálózati kapcsolat IP-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="4946c-119">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4946c-120">-Name</span></span>
<span data-ttu-id="4946c-121">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4946c-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="4946c-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="4946c-123">Virtuális gép hálózati felületének neve.</span><span class="sxs-lookup"><span data-stu-id="4946c-123">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4946c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4946c-125">Annak a csoportnak a neve, amely a parancsmag által beolvasott nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4946c-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="4946c-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="4946c-127">Virtuális gép indexe.</span><span class="sxs-lookup"><span data-stu-id="4946c-127">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4946c-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="4946c-129">Virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="4946c-129">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4946c-130">CommonParameters</span></span>
<span data-ttu-id="4946c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4946c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4946c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4946c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4946c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4946c-133">INPUTS</span></span>

### <span data-ttu-id="4946c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4946c-134">System.String</span></span>

## <span data-ttu-id="4946c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4946c-135">OUTPUTS</span></span>

### <span data-ttu-id="4946c-136">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4946c-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="4946c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4946c-137">NOTES</span></span>

## <span data-ttu-id="4946c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4946c-138">RELATED LINKS</span></span>

[<span data-ttu-id="4946c-139">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4946c-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="4946c-140">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4946c-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="4946c-141">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4946c-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


