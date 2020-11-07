---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841605"
---
# <span data-ttu-id="38b2f-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38b2f-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="38b2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="38b2f-103">Hálózati felületet kap.</span><span class="sxs-lookup"><span data-stu-id="38b2f-103">Gets a network interface.</span></span>

## <span data-ttu-id="38b2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38b2f-104">SYNTAX</span></span>

### <span data-ttu-id="38b2f-105">NoExpandStandAloneNic (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38b2f-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b2f-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="38b2f-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b2f-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="38b2f-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b2f-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="38b2f-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38b2f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="38b2f-109">DESCRIPTION</span></span>
<span data-ttu-id="38b2f-110">A **Get-AzNetworkInterface** parancsmag Azure-hálózati felületet vagy Azure hálózati felületek listáját tartalmazza egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="38b2f-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="38b2f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="38b2f-111">EXAMPLES</span></span>

### <span data-ttu-id="38b2f-112">1. példa: az összes hálózati kapcsolat beolvasása</span><span class="sxs-lookup"><span data-stu-id="38b2f-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="38b2f-113">Ez a parancs a jelenlegi előfizetés összes hálózati csatolóját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="38b2f-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="38b2f-114">2. példa: az összes hálózati kapcsolat beszerzése meghatározott kiépítési állapottal</span><span class="sxs-lookup"><span data-stu-id="38b2f-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="38b2f-115">Ez a parancs a ResourceGroup1 nevű erőforráscsoport minden hálózati csatolóját beilleszti a sikeres kiépítési állapotú erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="38b2f-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="38b2f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38b2f-116">PARAMETERS</span></span>

### <span data-ttu-id="38b2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b2f-117">-DefaultProfile</span></span>
<span data-ttu-id="38b2f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38b2f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38b2f-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="38b2f-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b2f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38b2f-120">-Name</span></span>
<span data-ttu-id="38b2f-121">Itt adhatja meg annak a hálózati kapcsolatnak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="38b2f-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="38b2f-123">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyből ez a parancsmag hálózati csatolókat kap.</span><span class="sxs-lookup"><span data-stu-id="38b2f-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b2f-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="38b2f-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="38b2f-125">Annak a virtuális gép-készletnek a virtuális gép indexét adja meg, amelyből ez a parancsmag hálózati illesztőfelületeket kap.</span><span class="sxs-lookup"><span data-stu-id="38b2f-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b2f-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="38b2f-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="38b2f-127">Annak a virtuális gépcsoport-készletnek a nevét adja meg, amelyből ez a parancsmag hálózati illesztőfelületet kap.</span><span class="sxs-lookup"><span data-stu-id="38b2f-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b2f-128">CommonParameters</span></span>
<span data-ttu-id="38b2f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38b2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b2f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b2f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b2f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38b2f-131">INPUTS</span></span>

## <span data-ttu-id="38b2f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38b2f-132">OUTPUTS</span></span>

### <span data-ttu-id="38b2f-133">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38b2f-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="38b2f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38b2f-134">NOTES</span></span>

## <span data-ttu-id="38b2f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38b2f-135">RELATED LINKS</span></span>

[<span data-ttu-id="38b2f-136">Új – AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38b2f-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="38b2f-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38b2f-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="38b2f-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38b2f-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


