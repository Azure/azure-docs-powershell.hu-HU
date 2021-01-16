---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476625"
---
# <span data-ttu-id="139f2-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="139f2-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="139f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="139f2-102">SYNOPSIS</span></span>
<span data-ttu-id="139f2-103">Létrehoz egy új sql virtuális gépcsoportot.</span><span class="sxs-lookup"><span data-stu-id="139f2-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="139f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="139f2-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="139f2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="139f2-105">DESCRIPTION</span></span>
<span data-ttu-id="139f2-106">A New-AzSqlVMGroup parancsmag létrehoz egy Azure SQL virtuális gépcsoportot.</span><span class="sxs-lookup"><span data-stu-id="139f2-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="139f2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="139f2-107">EXAMPLES</span></span>

### <span data-ttu-id="139f2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="139f2-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="139f2-109">Létrehoz egy új Azure SQL virtuális gépcsoportot, amely az ResourceGroup01 erőforráscsoport tesztcsoport-virtuális gépét használja.</span><span class="sxs-lookup"><span data-stu-id="139f2-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="139f2-110">$profile Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile típusú objektum</span><span class="sxs-lookup"><span data-stu-id="139f2-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="139f2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="139f2-111">PARAMETERS</span></span>

### <span data-ttu-id="139f2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="139f2-112">-AsJob</span></span>
<span data-ttu-id="139f2-113">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="139f2-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="139f2-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="139f2-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="139f2-115">A fürt létrehozásához használt név</span><span class="sxs-lookup"><span data-stu-id="139f2-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="139f2-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="139f2-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="139f2-117">Az operációs fürthöz használt név</span><span class="sxs-lookup"><span data-stu-id="139f2-117">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139f2-118">-DefaultProfile</span></span>
<span data-ttu-id="139f2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="139f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="139f2-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="139f2-120">-DomainFqdn</span></span>
<span data-ttu-id="139f2-121">A tartomány teljes neve</span><span class="sxs-lookup"><span data-stu-id="139f2-121">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="139f2-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="139f2-123">Választható elérési út a fájlmegosztáshoz</span><span class="sxs-lookup"><span data-stu-id="139f2-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="139f2-124">-Location</span><span class="sxs-lookup"><span data-stu-id="139f2-124">-Location</span></span>
<span data-ttu-id="139f2-125">SQL virtuális gépcsoport helye.</span><span class="sxs-lookup"><span data-stu-id="139f2-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="139f2-126">-Name</span></span>
<span data-ttu-id="139f2-127">SQL virtuális gépcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="139f2-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-128">-Offer</span><span class="sxs-lookup"><span data-stu-id="139f2-128">-Offer</span></span>
<span data-ttu-id="139f2-129">SQL virtuális gépcsoport ajánlata.</span><span class="sxs-lookup"><span data-stu-id="139f2-129">SQL virtual machine group offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="139f2-130">-OuPath</span></span>
<span data-ttu-id="139f2-131">A szervezeti egység útvonala, amelyben a csomópontok és a fürt meg fog jelenni</span><span class="sxs-lookup"><span data-stu-id="139f2-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="139f2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="139f2-132">-ResourceGroupName</span></span>
<span data-ttu-id="139f2-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="139f2-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-134">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="139f2-134">-Sku</span></span>
<span data-ttu-id="139f2-135">SQL virtuális gépcsoport kiadásának típusa.</span><span class="sxs-lookup"><span data-stu-id="139f2-135">SQL virtual machine group edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="139f2-136">-SqlServiceAccount</span></span>
<span data-ttu-id="139f2-137">Annak a névnek a neve, amely alatt az SQL-szolgáltatás a fürtben lévő összes részt vevő SQL-virtuális gépen futni fog</span><span class="sxs-lookup"><span data-stu-id="139f2-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="139f2-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="139f2-139">A tárolófiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="139f2-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="139f2-140">-StorageAccountUrl</span></span>
<span data-ttu-id="139f2-141">A tárolófiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="139f2-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139f2-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="139f2-142">-Tag</span></span>
<span data-ttu-id="139f2-143">Az SQL virtuális gépcsoporttal társítva lévő címkék.</span><span class="sxs-lookup"><span data-stu-id="139f2-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="139f2-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="139f2-144">-Confirm</span></span>
<span data-ttu-id="139f2-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="139f2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="139f2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="139f2-146">-WhatIf</span></span>
<span data-ttu-id="139f2-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="139f2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="139f2-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="139f2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="139f2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139f2-149">CommonParameters</span></span>
<span data-ttu-id="139f2-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="139f2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139f2-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="139f2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139f2-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="139f2-152">INPUTS</span></span>

### <span data-ttu-id="139f2-153">System.String</span><span class="sxs-lookup"><span data-stu-id="139f2-153">System.String</span></span>

## <span data-ttu-id="139f2-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="139f2-154">OUTPUTS</span></span>

### <span data-ttu-id="139f2-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="139f2-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="139f2-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="139f2-156">NOTES</span></span>

## <span data-ttu-id="139f2-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="139f2-157">RELATED LINKS</span></span>
