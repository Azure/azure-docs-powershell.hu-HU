---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209118"
---
# <span data-ttu-id="a0a84-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a0a84-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="a0a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0a84-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a84-103">Eltávolít egy Stack Edge-eszközt.</span><span class="sxs-lookup"><span data-stu-id="a0a84-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="a0a84-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0a84-104">SYNTAX</span></span>

### <span data-ttu-id="a0a84-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0a84-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a84-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a84-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a84-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a84-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a84-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0a84-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a84-109">A **Remove-AzStackEdgeDevice** parancsmag eltávolítja a Stack Edge-eszközök konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a0a84-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="a0a84-110">Felhívjuk a figyelmét arra, hogy az eszköz csak azt követően törölhető, hogy Ön elhelyezte a rendelést, és mielőtt a Microsoft felkészíti az eszközt a szállításra.</span><span class="sxs-lookup"><span data-stu-id="a0a84-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="a0a84-111">A parancsmag használata előtt olvassa el az erőforrás törléséről a [dokumentációt](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="a0a84-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="a0a84-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0a84-112">EXAMPLES</span></span>

### <span data-ttu-id="a0a84-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="a0a84-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="a0a84-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0a84-114">PARAMETERS</span></span>

### <span data-ttu-id="a0a84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0a84-115">-AsJob</span></span>
<span data-ttu-id="a0a84-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a0a84-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a84-117">-DefaultProfile</span></span>
<span data-ttu-id="a0a84-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0a84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a0a84-119">-DeviceObject</span></span>
<span data-ttu-id="a0a84-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="a0a84-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0a84-121">-Name</span></span>
<span data-ttu-id="a0a84-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a0a84-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0a84-123">-PassThru</span></span>
<span data-ttu-id="a0a84-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="a0a84-124">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a84-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0a84-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a0a84-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a84-127">-ResourceId</span></span>
<span data-ttu-id="a0a84-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a84-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0a84-129">-Confirm</span></span>
<span data-ttu-id="a0a84-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0a84-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a84-131">-WhatIf</span></span>
<span data-ttu-id="a0a84-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a0a84-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0a84-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0a84-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a84-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a84-134">CommonParameters</span></span>
<span data-ttu-id="a0a84-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a84-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a84-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0a84-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a84-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0a84-137">INPUTS</span></span>

### <span data-ttu-id="a0a84-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a0a84-138">System.String</span></span>

### <span data-ttu-id="a0a84-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a0a84-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a0a84-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0a84-140">OUTPUTS</span></span>

### <span data-ttu-id="a0a84-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0a84-141">System.Boolean</span></span>

## <span data-ttu-id="a0a84-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0a84-142">NOTES</span></span>

## <span data-ttu-id="a0a84-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0a84-143">RELATED LINKS</span></span>
