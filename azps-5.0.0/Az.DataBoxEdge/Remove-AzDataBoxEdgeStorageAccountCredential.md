---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 00cfc136465cc250d068344158d66f98dc6e0704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298694"
---
# <span data-ttu-id="eaf60-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="eaf60-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="eaf60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eaf60-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf60-103">Eltávolít egy eszköz tárolási fiókjának hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="eaf60-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="eaf60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eaf60-104">SYNTAX</span></span>

### <span data-ttu-id="eaf60-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eaf60-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaf60-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf60-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf60-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf60-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf60-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eaf60-108">DESCRIPTION</span></span>
<span data-ttu-id="eaf60-109">A **Remove-AzDataBoxEdgeStorageAccountCredential** parancsmag eltávolítja a tárolási fiók hitelesítő adatait egy adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="eaf60-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="eaf60-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eaf60-110">EXAMPLES</span></span>

### <span data-ttu-id="eaf60-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eaf60-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="eaf60-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eaf60-112">PARAMETERS</span></span>

### <span data-ttu-id="eaf60-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaf60-113">-AsJob</span></span>
<span data-ttu-id="eaf60-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eaf60-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaf60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf60-115">-DefaultProfile</span></span>
<span data-ttu-id="eaf60-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eaf60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf60-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eaf60-117">-DeviceName</span></span>
<span data-ttu-id="eaf60-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="eaf60-118">Device Name</span></span>

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

### <span data-ttu-id="eaf60-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eaf60-119">-InputObject</span></span>
<span data-ttu-id="eaf60-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="eaf60-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf60-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eaf60-121">-Name</span></span>
<span data-ttu-id="eaf60-122">A használandó tárterület-fiók neve</span><span class="sxs-lookup"><span data-stu-id="eaf60-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf60-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eaf60-123">-PassThru</span></span>
<span data-ttu-id="eaf60-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="eaf60-124">returns true if successful</span></span>

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

### <span data-ttu-id="eaf60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf60-125">-ResourceGroupName</span></span>
<span data-ttu-id="eaf60-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="eaf60-126">Resource Group Name</span></span>

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

### <span data-ttu-id="eaf60-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaf60-127">-ResourceId</span></span>
<span data-ttu-id="eaf60-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaf60-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf60-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eaf60-129">-Confirm</span></span>
<span data-ttu-id="eaf60-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eaf60-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf60-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf60-131">-WhatIf</span></span>
<span data-ttu-id="eaf60-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eaf60-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaf60-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eaf60-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf60-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf60-134">CommonParameters</span></span>
<span data-ttu-id="eaf60-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eaf60-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf60-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eaf60-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf60-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaf60-137">INPUTS</span></span>

### <span data-ttu-id="eaf60-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eaf60-138">System.String</span></span>

### <span data-ttu-id="eaf60-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="eaf60-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="eaf60-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaf60-140">OUTPUTS</span></span>

### <span data-ttu-id="eaf60-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eaf60-141">System.Boolean</span></span>

## <span data-ttu-id="eaf60-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eaf60-142">NOTES</span></span>

## <span data-ttu-id="eaf60-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eaf60-143">RELATED LINKS</span></span>
