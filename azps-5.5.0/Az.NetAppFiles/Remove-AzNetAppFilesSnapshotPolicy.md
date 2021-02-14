---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161251"
---
# <span data-ttu-id="f38c8-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f38c8-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f38c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f38c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f38c8-103">Törli az Azure NetApp-fájlok (ANF) pillanatkép-házirendet.</span><span class="sxs-lookup"><span data-stu-id="f38c8-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="f38c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f38c8-104">SYNTAX</span></span>

### <span data-ttu-id="f38c8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f38c8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f38c8-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38c8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f38c8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38c8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f38c8-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38c8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f38c8-109">DESCRIPTION</span></span>
<span data-ttu-id="f38c8-110">A **Remove-AzNetAppFilesSnapshotPolicy** parancsmag egy ANF-pillanatfelvételi házirendet töröl.</span><span class="sxs-lookup"><span data-stu-id="f38c8-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="f38c8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f38c8-111">EXAMPLES</span></span>

### <span data-ttu-id="f38c8-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f38c8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="f38c8-113">Ez a parancs törli az új ANF biztonsági mentési házirendet "MyBackupPolicy" néven a "MyAccount" fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f38c8-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="f38c8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f38c8-114">PARAMETERS</span></span>

### <span data-ttu-id="f38c8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f38c8-115">-AccountName</span></span>
<span data-ttu-id="f38c8-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="f38c8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f38c8-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f38c8-117">-AccountObject</span></span>
<span data-ttu-id="f38c8-118">The Account for the new Snapshot Policy object</span><span class="sxs-lookup"><span data-stu-id="f38c8-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="f38c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38c8-119">-DefaultProfile</span></span>
<span data-ttu-id="f38c8-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f38c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f38c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f38c8-121">-InputObject</span></span>
<span data-ttu-id="f38c8-122">Az eltávolítható SnapshotPolicy objektum</span><span class="sxs-lookup"><span data-stu-id="f38c8-122">The SnapshotPolicy object to remove</span></span>

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

### <span data-ttu-id="f38c8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f38c8-123">-Name</span></span>
<span data-ttu-id="f38c8-124">Az ANF pillanatkép-házirend neve</span><span class="sxs-lookup"><span data-stu-id="f38c8-124">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="f38c8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f38c8-125">-PassThru</span></span>
<span data-ttu-id="f38c8-126">Annak visszaadése, hogy a megadott fiók eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="f38c8-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="f38c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="f38c8-128">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="f38c8-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f38c8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f38c8-129">-ResourceId</span></span>
<span data-ttu-id="f38c8-130">Az ANF pillanatkép-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f38c8-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="f38c8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f38c8-131">-Confirm</span></span>
<span data-ttu-id="f38c8-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f38c8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38c8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38c8-133">-WhatIf</span></span>
<span data-ttu-id="f38c8-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f38c8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38c8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f38c8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f38c8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38c8-136">CommonParameters</span></span>
<span data-ttu-id="f38c8-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f38c8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38c8-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f38c8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38c8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f38c8-139">INPUTS</span></span>

### <span data-ttu-id="f38c8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f38c8-140">System.String</span></span>

### <span data-ttu-id="f38c8-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f38c8-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f38c8-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f38c8-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f38c8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f38c8-143">OUTPUTS</span></span>

### <span data-ttu-id="f38c8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="f38c8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="f38c8-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f38c8-145">NOTES</span></span>

## <span data-ttu-id="f38c8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f38c8-146">RELATED LINKS</span></span>
