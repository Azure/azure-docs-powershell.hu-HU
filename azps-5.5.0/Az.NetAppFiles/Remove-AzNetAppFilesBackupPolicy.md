---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203303"
---
# <span data-ttu-id="1a385-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a385-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="1a385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a385-102">SYNOPSIS</span></span>
<span data-ttu-id="1a385-103">Törli az Azure NetApp-fájlok (ANF) biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="1a385-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="1a385-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a385-104">SYNTAX</span></span>

### <span data-ttu-id="1a385-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a385-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a385-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a385-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a385-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a385-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a385-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a385-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a385-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a385-109">DESCRIPTION</span></span>
<span data-ttu-id="1a385-110">A **Remove-AzNetAppFilesBackupPolicy** parancsmag törli az ANF biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="1a385-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="1a385-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a385-111">EXAMPLES</span></span>

### <span data-ttu-id="1a385-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1a385-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="1a385-113">Ez a parancs törli az új ANF biztonsági mentési házirendet "MyBackupPolicy" néven a "MyAccount" fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1a385-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="1a385-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a385-114">PARAMETERS</span></span>

### <span data-ttu-id="1a385-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a385-115">-AccountName</span></span>
<span data-ttu-id="1a385-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1a385-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="1a385-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1a385-117">-AccountObject</span></span>
<span data-ttu-id="1a385-118">Az eltávolítható biztonsági mentési házirendet tartalmazó Fiók objektum</span><span class="sxs-lookup"><span data-stu-id="1a385-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="1a385-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a385-119">-DefaultProfile</span></span>
<span data-ttu-id="1a385-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a385-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a385-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a385-121">-InputObject</span></span>
<span data-ttu-id="1a385-122">Az eltávolítható BackupPolicy objektum</span><span class="sxs-lookup"><span data-stu-id="1a385-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a385-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1a385-123">-Name</span></span>
<span data-ttu-id="1a385-124">Az ANF biztonsági mentési házirend neve</span><span class="sxs-lookup"><span data-stu-id="1a385-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a385-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a385-125">-PassThru</span></span>
<span data-ttu-id="1a385-126">Annak visszaadése, hogy a megadott biztonságimásolat-házirend eltávolítása sikeresen megtörtént-e</span><span class="sxs-lookup"><span data-stu-id="1a385-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="1a385-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a385-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a385-128">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="1a385-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1a385-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a385-129">-ResourceId</span></span>
<span data-ttu-id="1a385-130">Az ANF biztonsági mentési házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1a385-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="1a385-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a385-131">-Confirm</span></span>
<span data-ttu-id="1a385-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1a385-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a385-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a385-133">-WhatIf</span></span>
<span data-ttu-id="1a385-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1a385-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a385-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a385-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a385-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a385-136">CommonParameters</span></span>
<span data-ttu-id="1a385-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a385-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a385-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a385-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a385-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a385-139">INPUTS</span></span>

### <span data-ttu-id="1a385-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1a385-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="1a385-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1a385-141">System.String</span></span>

### <span data-ttu-id="1a385-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a385-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="1a385-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a385-143">OUTPUTS</span></span>

### <span data-ttu-id="1a385-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1a385-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="1a385-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a385-145">NOTES</span></span>

## <span data-ttu-id="1a385-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a385-146">RELATED LINKS</span></span>
