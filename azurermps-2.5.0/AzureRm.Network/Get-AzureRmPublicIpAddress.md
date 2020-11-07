---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 1404acfa32de79096e990adbe2f66b43af0d4e96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850690"
---
# <span data-ttu-id="07a99-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="07a99-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="07a99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07a99-102">SYNOPSIS</span></span>
<span data-ttu-id="07a99-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="07a99-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07a99-104">SYNTAX</span></span>

### <span data-ttu-id="07a99-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07a99-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07a99-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="07a99-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07a99-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="07a99-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07a99-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="07a99-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07a99-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="07a99-109">DESCRIPTION</span></span>
<span data-ttu-id="07a99-110">A **Get-AzureRmPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="07a99-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="07a99-111">Példák</span><span class="sxs-lookup"><span data-stu-id="07a99-111">EXAMPLES</span></span>

### <span data-ttu-id="07a99-112">1: nyilvános IP-erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="07a99-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="07a99-113">Ez a parancs olyan nyilvános IP-cím típusú erőforrást kap, amelyben a név $publicIPName szerepel az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="07a99-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="07a99-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07a99-114">PARAMETERS</span></span>

### <span data-ttu-id="07a99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a99-115">-DefaultProfile</span></span>
<span data-ttu-id="07a99-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07a99-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="07a99-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="07a99-118">-IpConfigurationName</span></span>
<span data-ttu-id="07a99-119">Hálózati kapcsolat IP-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="07a99-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07a99-120">-Name</span></span>
<span data-ttu-id="07a99-121">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="07a99-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="07a99-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="07a99-123">Virtuális gép hálózati felületének neve.</span><span class="sxs-lookup"><span data-stu-id="07a99-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a99-124">-ResourceGroupName</span></span>
<span data-ttu-id="07a99-125">Annak a csoportnak a neve, amely a parancsmag által beolvasott nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="07a99-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="07a99-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="07a99-127">Virtuális gép indexe.</span><span class="sxs-lookup"><span data-stu-id="07a99-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="07a99-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="07a99-129">Virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="07a99-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a99-130">CommonParameters</span></span>
<span data-ttu-id="07a99-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07a99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a99-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a99-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a99-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a99-133">INPUTS</span></span>

## <span data-ttu-id="07a99-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a99-134">OUTPUTS</span></span>

### <span data-ttu-id="07a99-135">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="07a99-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="07a99-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07a99-136">NOTES</span></span>

## <span data-ttu-id="07a99-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07a99-137">RELATED LINKS</span></span>

[<span data-ttu-id="07a99-138">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="07a99-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="07a99-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="07a99-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="07a99-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="07a99-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


