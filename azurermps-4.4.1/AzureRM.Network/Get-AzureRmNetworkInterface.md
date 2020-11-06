---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 42d5ef31b49f8abe5c8e582e0a85e8766a71b9a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504064"
---
# <span data-ttu-id="e6ccf-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6ccf-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="e6ccf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ccf-103">Hálózati felületet kap.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6ccf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6ccf-104">SYNTAX</span></span>

### <span data-ttu-id="e6ccf-105">NoExpandStandAloneNic (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6ccf-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ccf-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="e6ccf-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ccf-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="e6ccf-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ccf-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="e6ccf-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6ccf-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6ccf-109">DESCRIPTION</span></span>
<span data-ttu-id="e6ccf-110">A **Get-AzureRmNetworkInterface** parancsmag Azure-hálózati felületet vagy Azure hálózati felületek listáját tartalmazza egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="e6ccf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e6ccf-111">EXAMPLES</span></span>

### <span data-ttu-id="e6ccf-112">1. példa: az összes hálózati kapcsolat beolvasása</span><span class="sxs-lookup"><span data-stu-id="e6ccf-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="e6ccf-113">Ez a parancs a jelenlegi előfizetés összes hálózati csatolóját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="e6ccf-114">2. példa: az összes hálózati kapcsolat beszerzése meghatározott kiépítési állapottal</span><span class="sxs-lookup"><span data-stu-id="e6ccf-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="e6ccf-115">Ez a parancs a ResourceGroup1 nevű erőforráscsoport minden hálózati csatolóját beilleszti a sikeres kiépítési állapotú erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="e6ccf-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6ccf-116">PARAMETERS</span></span>

### <span data-ttu-id="e6ccf-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e6ccf-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ccf-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6ccf-118">-Name</span></span>
<span data-ttu-id="e6ccf-119">Itt adhatja meg annak a hálózati kapcsolatnak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-119">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ccf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ccf-120">-ResourceGroupName</span></span>
<span data-ttu-id="e6ccf-121">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyből ez a parancsmag hálózati csatolókat kap.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-121">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ccf-122">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="e6ccf-122">-VirtualMachineIndex</span></span>
<span data-ttu-id="e6ccf-123">Annak a virtuális gép-készletnek a virtuális gép indexét adja meg, amelyből ez a parancsmag hálózati illesztőfelületeket kap.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-123">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ccf-124">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e6ccf-124">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="e6ccf-125">Annak a virtuális gépcsoport-készletnek a nevét adja meg, amelyből ez a parancsmag hálózati illesztőfelületet kap.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-125">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ccf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ccf-126">-DefaultProfile</span></span>
<span data-ttu-id="e6ccf-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6ccf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6ccf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ccf-128">CommonParameters</span></span>
<span data-ttu-id="e6ccf-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6ccf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ccf-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ccf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ccf-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ccf-131">INPUTS</span></span>

## <span data-ttu-id="e6ccf-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ccf-132">OUTPUTS</span></span>

### <span data-ttu-id="e6ccf-133">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6ccf-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e6ccf-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6ccf-134">NOTES</span></span>

## <span data-ttu-id="e6ccf-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6ccf-135">RELATED LINKS</span></span>

[<span data-ttu-id="e6ccf-136">Új – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6ccf-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="e6ccf-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6ccf-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="e6ccf-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6ccf-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


