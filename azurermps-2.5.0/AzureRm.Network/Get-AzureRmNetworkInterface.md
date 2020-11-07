---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850713"
---
# <span data-ttu-id="d616b-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d616b-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="d616b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d616b-102">SYNOPSIS</span></span>
<span data-ttu-id="d616b-103">Hálózati felületet kap.</span><span class="sxs-lookup"><span data-stu-id="d616b-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d616b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d616b-104">SYNTAX</span></span>

### <span data-ttu-id="d616b-105">NoExpandStandAloneNic (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d616b-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d616b-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="d616b-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d616b-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d616b-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d616b-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d616b-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d616b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d616b-109">DESCRIPTION</span></span>
<span data-ttu-id="d616b-110">A **Get-AzureRmNetworkInterface** parancsmag Azure-hálózati felületet vagy Azure hálózati felületek listáját tartalmazza egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="d616b-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="d616b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d616b-111">EXAMPLES</span></span>

### <span data-ttu-id="d616b-112">1. példa: az összes hálózati kapcsolat beolvasása</span><span class="sxs-lookup"><span data-stu-id="d616b-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="d616b-113">Ez a parancs a jelenlegi előfizetés összes hálózati csatolóját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d616b-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="d616b-114">2. példa: az összes hálózati kapcsolat beszerzése meghatározott kiépítési állapottal</span><span class="sxs-lookup"><span data-stu-id="d616b-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="d616b-115">Ez a parancs a ResourceGroup1 nevű erőforráscsoport minden hálózati csatolóját beilleszti a sikeres kiépítési állapotú erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="d616b-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="d616b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d616b-116">PARAMETERS</span></span>

### <span data-ttu-id="d616b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d616b-117">-DefaultProfile</span></span>
<span data-ttu-id="d616b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d616b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d616b-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d616b-119">-ExpandResource</span></span>
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

### <span data-ttu-id="d616b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d616b-120">-Name</span></span>
<span data-ttu-id="d616b-121">Itt adhatja meg annak a hálózati kapcsolatnak a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d616b-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d616b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d616b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d616b-123">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyből ez a parancsmag hálózati csatolókat kap.</span><span class="sxs-lookup"><span data-stu-id="d616b-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="d616b-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="d616b-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="d616b-125">Annak a virtuális gép-készletnek a virtuális gép indexét adja meg, amelyből ez a parancsmag hálózati illesztőfelületeket kap.</span><span class="sxs-lookup"><span data-stu-id="d616b-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="d616b-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d616b-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d616b-127">Annak a virtuális gépcsoport-készletnek a nevét adja meg, amelyből ez a parancsmag hálózati illesztőfelületet kap.</span><span class="sxs-lookup"><span data-stu-id="d616b-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="d616b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d616b-128">CommonParameters</span></span>
<span data-ttu-id="d616b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d616b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d616b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d616b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d616b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d616b-131">INPUTS</span></span>

## <span data-ttu-id="d616b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d616b-132">OUTPUTS</span></span>

### <span data-ttu-id="d616b-133">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d616b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d616b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d616b-134">NOTES</span></span>

## <span data-ttu-id="d616b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d616b-135">RELATED LINKS</span></span>

[<span data-ttu-id="d616b-136">Új – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d616b-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="d616b-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d616b-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="d616b-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d616b-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


