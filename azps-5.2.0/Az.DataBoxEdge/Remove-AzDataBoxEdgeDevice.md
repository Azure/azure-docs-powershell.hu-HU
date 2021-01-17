---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343601"
---
# <span data-ttu-id="fdfd0-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fdfd0-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="fdfd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfd0-103">Eltávolít egy Data Box Edge-eszközt.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="fdfd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdfd0-104">SYNTAX</span></span>

### <span data-ttu-id="fdfd0-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdfd0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfd0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfd0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfd0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfd0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdfd0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdfd0-108">DESCRIPTION</span></span>
<span data-ttu-id="fdfd0-109">Az **Remove-AzDataBoxEdgeDevice** parancsmag eltávolítja az Adatmező-szegélyű eszközök konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="fdfd0-110">Felhívjuk a figyelmét arra, hogy az eszköz csak azt követően törölhető, hogy Ön elhelyezte a rendelést, és mielőtt a Microsoft felkészíti az eszközt a szállításra.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="fdfd0-111">A parancsmag használata előtt olvassa el az erőforrás törléséről a [dokumentációt](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="fdfd0-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="fdfd0-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdfd0-112">EXAMPLES</span></span>

### <span data-ttu-id="fdfd0-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="fdfd0-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="fdfd0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdfd0-114">PARAMETERS</span></span>

### <span data-ttu-id="fdfd0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdfd0-115">-AsJob</span></span>
<span data-ttu-id="fdfd0-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fdfd0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdfd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfd0-117">-DefaultProfile</span></span>
<span data-ttu-id="fdfd0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfd0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdfd0-119">-InputObject</span></span>
<span data-ttu-id="fdfd0-120">Bemeneti objektum</span><span class="sxs-lookup"><span data-stu-id="fdfd0-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdfd0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fdfd0-121">-Name</span></span>
<span data-ttu-id="fdfd0-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fdfd0-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdfd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdfd0-123">-PassThru</span></span>
<span data-ttu-id="fdfd0-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="fdfd0-124">returns true if successful</span></span>

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

### <span data-ttu-id="fdfd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="fdfd0-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fdfd0-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdfd0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfd0-127">-ResourceId</span></span>
<span data-ttu-id="fdfd0-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfd0-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="fdfd0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdfd0-129">-Confirm</span></span>
<span data-ttu-id="fdfd0-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfd0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfd0-131">-WhatIf</span></span>
<span data-ttu-id="fdfd0-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdfd0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfd0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfd0-134">CommonParameters</span></span>
<span data-ttu-id="fdfd0-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdfd0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfd0-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdfd0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfd0-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdfd0-137">INPUTS</span></span>

### <span data-ttu-id="fdfd0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fdfd0-138">System.String</span></span>

### <span data-ttu-id="fdfd0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fdfd0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="fdfd0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdfd0-140">OUTPUTS</span></span>

### <span data-ttu-id="fdfd0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fdfd0-141">System.Boolean</span></span>

## <span data-ttu-id="fdfd0-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdfd0-142">NOTES</span></span>

## <span data-ttu-id="fdfd0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdfd0-143">RELATED LINKS</span></span>
