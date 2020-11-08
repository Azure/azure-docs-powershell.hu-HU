---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183840"
---
# <span data-ttu-id="97d04-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="97d04-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="97d04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97d04-102">SYNOPSIS</span></span>
<span data-ttu-id="97d04-103">SQL-virtuálisgép-csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="97d04-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="97d04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97d04-104">SYNTAX</span></span>

### <span data-ttu-id="97d04-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97d04-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97d04-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="97d04-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97d04-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="97d04-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97d04-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="97d04-108">DESCRIPTION</span></span>
<span data-ttu-id="97d04-109">Az Update-AzSqlVMGroup parancsmag frissíti egy virtuális SQL Machine-csoportot.</span><span class="sxs-lookup"><span data-stu-id="97d04-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="97d04-110">Példák</span><span class="sxs-lookup"><span data-stu-id="97d04-110">EXAMPLES</span></span>

### <span data-ttu-id="97d04-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97d04-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="97d04-112">Frissíti egy virtuális SQL Machine-csoport címkéit.</span><span class="sxs-lookup"><span data-stu-id="97d04-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="97d04-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97d04-113">PARAMETERS</span></span>

### <span data-ttu-id="97d04-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97d04-114">-AsJob</span></span>
<span data-ttu-id="97d04-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="97d04-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="97d04-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="97d04-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="97d04-117">A fürtök létrehozásához használt név</span><span class="sxs-lookup"><span data-stu-id="97d04-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="97d04-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="97d04-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="97d04-119">Az üzemeltetési fürtökhöz használt név</span><span class="sxs-lookup"><span data-stu-id="97d04-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="97d04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d04-120">-DefaultProfile</span></span>
<span data-ttu-id="97d04-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97d04-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97d04-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="97d04-122">-DomainFqdn</span></span>
<span data-ttu-id="97d04-123">A tartomány teljesen minősített neve</span><span class="sxs-lookup"><span data-stu-id="97d04-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="97d04-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="97d04-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="97d04-125">A fájlmegosztásról választható elérési útja</span><span class="sxs-lookup"><span data-stu-id="97d04-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="97d04-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97d04-126">-InputObject</span></span>
<span data-ttu-id="97d04-127">Virtuális SQL Machine-objektum.</span><span class="sxs-lookup"><span data-stu-id="97d04-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="97d04-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97d04-128">-Name</span></span>
<span data-ttu-id="97d04-129">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="97d04-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="97d04-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="97d04-130">-OuPath</span></span>
<span data-ttu-id="97d04-131">Szervezeti egység elérési útvonala, amelyben a csomópontok és a klaszterek jelen lesznek</span><span class="sxs-lookup"><span data-stu-id="97d04-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="97d04-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97d04-132">-ResourceGroupName</span></span>
<span data-ttu-id="97d04-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="97d04-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="97d04-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97d04-134">-ResourceId</span></span>
<span data-ttu-id="97d04-135">SQL virtuálisgép-csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97d04-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="97d04-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="97d04-136">-SqlServiceAccount</span></span>
<span data-ttu-id="97d04-137">A fürtben a többi SQL-szolgáltatónál futtatandó SQL-szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="97d04-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="97d04-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="97d04-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="97d04-139">A tanú-tároló fiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="97d04-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="97d04-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="97d04-140">-StorageAccountUrl</span></span>
<span data-ttu-id="97d04-141">A tanú-tároló fiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="97d04-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="97d04-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="97d04-142">-Tag</span></span>
<span data-ttu-id="97d04-143">A virtuális SQL Machine-csoporttal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="97d04-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="97d04-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97d04-144">-Confirm</span></span>
<span data-ttu-id="97d04-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97d04-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97d04-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97d04-146">-WhatIf</span></span>
<span data-ttu-id="97d04-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97d04-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97d04-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97d04-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97d04-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d04-149">CommonParameters</span></span>
<span data-ttu-id="97d04-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97d04-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d04-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97d04-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d04-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97d04-152">INPUTS</span></span>

### <span data-ttu-id="97d04-153">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="97d04-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="97d04-154">System. String</span><span class="sxs-lookup"><span data-stu-id="97d04-154">System.String</span></span>

## <span data-ttu-id="97d04-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97d04-155">OUTPUTS</span></span>

### <span data-ttu-id="97d04-156">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="97d04-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="97d04-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97d04-157">NOTES</span></span>

## <span data-ttu-id="97d04-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97d04-158">RELATED LINKS</span></span>
