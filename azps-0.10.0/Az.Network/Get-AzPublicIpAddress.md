---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841530"
---
# <span data-ttu-id="fd7a9-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd7a9-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="fd7a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7a9-103">Nyilvános IP-címet kap.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-103">Gets a public IP address.</span></span>

## <span data-ttu-id="fd7a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd7a9-104">SYNTAX</span></span>

### <span data-ttu-id="fd7a9-105">NoExpandStandAloneIp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd7a9-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7a9-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="fd7a9-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7a9-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="fd7a9-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7a9-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="fd7a9-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd7a9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd7a9-109">DESCRIPTION</span></span>
<span data-ttu-id="fd7a9-110">A **Get-AzPublicIPAddress** parancsmag egy vagy több nyilvános IP-címet kap egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="fd7a9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fd7a9-111">EXAMPLES</span></span>

### <span data-ttu-id="fd7a9-112">1: nyilvános IP-erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="fd7a9-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="fd7a9-113">Ez a parancs olyan nyilvános IP-cím típusú erőforrást kap, amelyben a név $publicIPName szerepel az erőforráscsoport $rgName.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="fd7a9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd7a9-114">PARAMETERS</span></span>

### <span data-ttu-id="fd7a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7a9-115">-DefaultProfile</span></span>
<span data-ttu-id="fd7a9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7a9-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="fd7a9-117">-ExpandResource</span></span>
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

### <span data-ttu-id="fd7a9-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="fd7a9-118">-IpConfigurationName</span></span>
<span data-ttu-id="fd7a9-119">Hálózati kapcsolat IP-konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="fd7a9-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="fd7a9-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd7a9-120">-Name</span></span>
<span data-ttu-id="fd7a9-121">Annak a nyilvános IP-címnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fd7a9-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="fd7a9-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="fd7a9-123">Virtuális gép hálózati felületének neve.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="fd7a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd7a9-125">Annak a csoportnak a neve, amely a parancsmag által beolvasott nyilvános IP-címet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fd7a9-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="fd7a9-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="fd7a9-127">Virtuális gép indexe.</span><span class="sxs-lookup"><span data-stu-id="fd7a9-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="fd7a9-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fd7a9-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="fd7a9-129">Virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="fd7a9-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="fd7a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7a9-130">CommonParameters</span></span>
<span data-ttu-id="fd7a9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd7a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7a9-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7a9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7a9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7a9-133">INPUTS</span></span>

## <span data-ttu-id="fd7a9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7a9-134">OUTPUTS</span></span>

### <span data-ttu-id="fd7a9-135">Microsoft. Azure. commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd7a9-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fd7a9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd7a9-136">NOTES</span></span>

## <span data-ttu-id="fd7a9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd7a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="fd7a9-138">Új – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd7a9-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="fd7a9-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd7a9-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="fd7a9-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd7a9-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


