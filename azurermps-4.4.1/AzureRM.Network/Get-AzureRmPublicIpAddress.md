---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 9864ba724d20e088e410bc99e8642fae97d71fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503240"
---
# <span data-ttu-id="0af90-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0af90-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="0af90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0af90-102">SYNOPSIS</span></span>
<span data-ttu-id="0af90-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="0af90-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0af90-104">SYNTAX</span></span>

### <span data-ttu-id="0af90-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0af90-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af90-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="0af90-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af90-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="0af90-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af90-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="0af90-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af90-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0af90-109">DESCRIPTION</span></span>
<span data-ttu-id="0af90-110">A **Get-AzureRmPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="0af90-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="0af90-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0af90-111">EXAMPLES</span></span>

### <span data-ttu-id="0af90-112">1: nyilvános IP-erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="0af90-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="0af90-113">Ez a parancs olyan nyilvános IP-cím típusú erőforrást kap, amelyben a név $publicIPName szerepel az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="0af90-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="0af90-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0af90-114">PARAMETERS</span></span>

### <span data-ttu-id="0af90-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0af90-115">-ExpandResource</span></span>
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

### <span data-ttu-id="0af90-116">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0af90-116">-IpConfigurationName</span></span>
<span data-ttu-id="0af90-117">Hálózati kapcsolat IP-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="0af90-117">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="0af90-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0af90-118">-Name</span></span>
<span data-ttu-id="0af90-119">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="0af90-119">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0af90-120">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0af90-120">-NetworkInterfaceName</span></span>
<span data-ttu-id="0af90-121">Virtuális gép hálózati felületének neve.</span><span class="sxs-lookup"><span data-stu-id="0af90-121">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="0af90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af90-122">-ResourceGroupName</span></span>
<span data-ttu-id="0af90-123">Annak a csoportnak a neve, amely a parancsmag által beolvasott nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0af90-123">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0af90-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="0af90-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="0af90-125">Virtuális gép indexe.</span><span class="sxs-lookup"><span data-stu-id="0af90-125">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="0af90-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0af90-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="0af90-127">Virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="0af90-127">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="0af90-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af90-128">-DefaultProfile</span></span>
<span data-ttu-id="0af90-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0af90-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af90-130">CommonParameters</span></span>
<span data-ttu-id="0af90-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0af90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af90-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af90-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af90-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0af90-133">INPUTS</span></span>

## <span data-ttu-id="0af90-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0af90-134">OUTPUTS</span></span>

### <span data-ttu-id="0af90-135">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0af90-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0af90-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0af90-136">NOTES</span></span>

## <span data-ttu-id="0af90-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0af90-137">RELATED LINKS</span></span>

[<span data-ttu-id="0af90-138">Új – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0af90-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0af90-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0af90-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0af90-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0af90-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


