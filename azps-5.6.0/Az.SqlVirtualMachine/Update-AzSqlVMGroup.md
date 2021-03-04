---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 04a75ec50f985bb1cea0266c077946adbdab4f65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943290"
---
# <span data-ttu-id="ed8ad-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ed8ad-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="ed8ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8ad-103">Frissíti az sql virtuális gépcsoportot.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="ed8ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed8ad-104">SYNTAX</span></span>

### <span data-ttu-id="ed8ad-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed8ad-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed8ad-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8ad-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8ad-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8ad-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed8ad-108">DESCRIPTION</span></span>
<span data-ttu-id="ed8ad-109">A Update-AzSqlVMGroup parancsmag frissíti az sql virtuális gépcsoportot.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="ed8ad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed8ad-110">EXAMPLES</span></span>

### <span data-ttu-id="ed8ad-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ed8ad-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="ed8ad-112">Frissíti egy sql virtuális gépcsoport címkéit.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="ed8ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed8ad-113">PARAMETERS</span></span>

### <span data-ttu-id="ed8ad-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed8ad-114">-AsJob</span></span>
<span data-ttu-id="ed8ad-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ed8ad-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="ed8ad-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="ed8ad-117">A fürt létrehozásához használt név</span><span class="sxs-lookup"><span data-stu-id="ed8ad-117">Name used for creating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="ed8ad-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="ed8ad-119">Az operációs fürthöz használt név</span><span class="sxs-lookup"><span data-stu-id="ed8ad-119">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8ad-120">-DefaultProfile</span></span>
<span data-ttu-id="ed8ad-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8ad-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="ed8ad-122">-DomainFqdn</span></span>
<span data-ttu-id="ed8ad-123">A tartomány teljes neve</span><span class="sxs-lookup"><span data-stu-id="ed8ad-123">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="ed8ad-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="ed8ad-125">Választható elérési út a fájlmegosztáshoz</span><span class="sxs-lookup"><span data-stu-id="ed8ad-125">Optional path for fileshare witness</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8ad-126">-InputObject</span></span>
<span data-ttu-id="ed8ad-127">SQL virtuális gépobjektum.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ed8ad-128">-Name</span></span>
<span data-ttu-id="ed8ad-129">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="ed8ad-130">-OuPath</span></span>
<span data-ttu-id="ed8ad-131">A szervezeti egység útvonala, amelyben a csomópontok és a fürt meg fog jelenni</span><span class="sxs-lookup"><span data-stu-id="ed8ad-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8ad-132">-ResourceGroupName</span></span>
<span data-ttu-id="ed8ad-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8ad-134">-ResourceId</span></span>
<span data-ttu-id="ed8ad-135">SQL virtuális gépcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="ed8ad-136">-SqlServiceAccount</span></span>
<span data-ttu-id="ed8ad-137">Annak a névnek a neve, amely alatt az SQL-szolgáltatás a fürtben lévő összes részt vevő SQL-virtuális gépen futni fog</span><span class="sxs-lookup"><span data-stu-id="ed8ad-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ed8ad-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="ed8ad-139">A tárolófiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="ed8ad-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ed8ad-140">-StorageAccountUrl</span></span>
<span data-ttu-id="ed8ad-141">A tárolófiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="ed8ad-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed8ad-142">-Tag</span></span>
<span data-ttu-id="ed8ad-143">Az SQL virtuális gépcsoporttal társítva lévő címkék.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ad-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed8ad-144">-Confirm</span></span>
<span data-ttu-id="ed8ad-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8ad-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8ad-146">-WhatIf</span></span>
<span data-ttu-id="ed8ad-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8ad-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8ad-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8ad-149">CommonParameters</span></span>
<span data-ttu-id="ed8ad-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8ad-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed8ad-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8ad-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed8ad-152">INPUTS</span></span>

### <span data-ttu-id="ed8ad-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ed8ad-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="ed8ad-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ed8ad-154">System.String</span></span>

## <span data-ttu-id="ed8ad-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed8ad-155">OUTPUTS</span></span>

### <span data-ttu-id="ed8ad-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ed8ad-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ed8ad-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed8ad-157">NOTES</span></span>

## <span data-ttu-id="ed8ad-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed8ad-158">RELATED LINKS</span></span>
