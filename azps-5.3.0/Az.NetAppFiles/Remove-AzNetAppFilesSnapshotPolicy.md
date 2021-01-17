---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380602"
---
# <span data-ttu-id="ef3e2-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3e2-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ef3e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef3e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3e2-103">Törli az Azure NetApp-fájlok (ANF) pillanatkép-házirendet.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="ef3e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef3e2-104">SYNTAX</span></span>

### <span data-ttu-id="ef3e2-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef3e2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3e2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef3e2-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3e2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef3e2-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3e2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef3e2-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3e2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef3e2-109">DESCRIPTION</span></span>
<span data-ttu-id="ef3e2-110">A **Remove-AzNetAppFilesSnapshotPolicy** parancsmag törli az ANF pillanatkép-házirendet.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="ef3e2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef3e2-111">EXAMPLES</span></span>

### <span data-ttu-id="ef3e2-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ef3e2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="ef3e2-113">Ez a parancs törli az új ANF biztonsági mentési házirendet "MyBackupPolicy" néven a "MyAccount" fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="ef3e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef3e2-114">PARAMETERS</span></span>

### <span data-ttu-id="ef3e2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef3e2-115">-AccountName</span></span>
<span data-ttu-id="ef3e2-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="ef3e2-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ef3e2-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ef3e2-117">-AccountObject</span></span>
<span data-ttu-id="ef3e2-118">The Account for the new Snapshot Policy object</span><span class="sxs-lookup"><span data-stu-id="ef3e2-118">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef3e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3e2-119">-DefaultProfile</span></span>
<span data-ttu-id="ef3e2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef3e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef3e2-121">-InputObject</span></span>
<span data-ttu-id="ef3e2-122">Az eltávolítható SnapshotPolicy objektum</span><span class="sxs-lookup"><span data-stu-id="ef3e2-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef3e2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ef3e2-123">-Name</span></span>
<span data-ttu-id="ef3e2-124">Az ANF pillanatkép-házirend neve</span><span class="sxs-lookup"><span data-stu-id="ef3e2-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef3e2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef3e2-125">-PassThru</span></span>
<span data-ttu-id="ef3e2-126">Annak visszaadése, hogy a megadott fiók eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="ef3e2-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="ef3e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef3e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef3e2-128">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="ef3e2-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ef3e2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef3e2-129">-ResourceId</span></span>
<span data-ttu-id="ef3e2-130">Az ANF pillanatkép-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ef3e2-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="ef3e2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef3e2-131">-Confirm</span></span>
<span data-ttu-id="ef3e2-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3e2-133">-WhatIf</span></span>
<span data-ttu-id="ef3e2-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef3e2-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef3e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3e2-136">CommonParameters</span></span>
<span data-ttu-id="ef3e2-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef3e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3e2-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef3e2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3e2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef3e2-139">INPUTS</span></span>

### <span data-ttu-id="ef3e2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ef3e2-140">System.String</span></span>

### <span data-ttu-id="ef3e2-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ef3e2-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ef3e2-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3e2-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ef3e2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef3e2-143">OUTPUTS</span></span>

### <span data-ttu-id="ef3e2-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3e2-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ef3e2-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef3e2-145">NOTES</span></span>

## <span data-ttu-id="ef3e2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef3e2-146">RELATED LINKS</span></span>
