---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345210"
---
# <span data-ttu-id="2b73a-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="2b73a-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="2b73a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b73a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b73a-103">Törli az Azure NetApp-fájlok (ANF) pillanatképét.</span><span class="sxs-lookup"><span data-stu-id="2b73a-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="2b73a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b73a-104">SYNTAX</span></span>

### <span data-ttu-id="2b73a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b73a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b73a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b73a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b73a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b73a-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b73a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b73a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b73a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b73a-109">DESCRIPTION</span></span>
<span data-ttu-id="2b73a-110">A **Remove-AzNetAppFilesSnapshot** parancsmag törli az ANF-pillanatfelvételt.</span><span class="sxs-lookup"><span data-stu-id="2b73a-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="2b73a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b73a-111">EXAMPLES</span></span>

### <span data-ttu-id="2b73a-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2b73a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="2b73a-113">Ez a parancs törli a "MyAnfSnapshot" ANF-pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="2b73a-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="2b73a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b73a-114">PARAMETERS</span></span>

### <span data-ttu-id="2b73a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b73a-115">-AccountName</span></span>
<span data-ttu-id="2b73a-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2b73a-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b73a-117">-DefaultProfile</span></span>
<span data-ttu-id="2b73a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b73a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b73a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b73a-119">-InputObject</span></span>
<span data-ttu-id="2b73a-120">Az eltávolítható pillanatkép-objektum</span><span class="sxs-lookup"><span data-stu-id="2b73a-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b73a-121">-Name</span></span>
<span data-ttu-id="2b73a-122">Az ANF-pillanatkép neve</span><span class="sxs-lookup"><span data-stu-id="2b73a-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b73a-123">-PassThru</span></span>
<span data-ttu-id="2b73a-124">Visszaadja, hogy sikerült-e eltávolítani a megadott mennyiséget.</span><span class="sxs-lookup"><span data-stu-id="2b73a-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="2b73a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2b73a-125">-PoolName</span></span>
<span data-ttu-id="2b73a-126">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="2b73a-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b73a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b73a-128">Az ANF-pillanatfelvétel erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="2b73a-128">The resource group of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b73a-129">-ResourceId</span></span>
<span data-ttu-id="2b73a-130">Az ANF-pillanatfelvétel erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2b73a-130">The resource id of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="2b73a-131">-VolumeName</span></span>
<span data-ttu-id="2b73a-132">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="2b73a-132">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="2b73a-133">-VolumeObject</span></span>
<span data-ttu-id="2b73a-134">Az eltávolítható pillanatképet tartalmazó kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="2b73a-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b73a-135">-Confirm</span></span>
<span data-ttu-id="2b73a-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2b73a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b73a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b73a-137">-WhatIf</span></span>
<span data-ttu-id="2b73a-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2b73a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b73a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b73a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b73a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b73a-140">CommonParameters</span></span>
<span data-ttu-id="2b73a-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b73a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b73a-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b73a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b73a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b73a-143">INPUTS</span></span>

### <span data-ttu-id="2b73a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2b73a-144">System.String</span></span>

### <span data-ttu-id="2b73a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2b73a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="2b73a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="2b73a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="2b73a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b73a-147">OUTPUTS</span></span>

### <span data-ttu-id="2b73a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b73a-148">System.Boolean</span></span>

## <span data-ttu-id="2b73a-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b73a-149">NOTES</span></span>

## <span data-ttu-id="2b73a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b73a-150">RELATED LINKS</span></span>
