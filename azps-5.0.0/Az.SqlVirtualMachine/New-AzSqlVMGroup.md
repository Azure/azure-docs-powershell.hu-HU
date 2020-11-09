---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300077"
---
# <span data-ttu-id="160c6-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="160c6-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="160c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="160c6-102">SYNOPSIS</span></span>
<span data-ttu-id="160c6-103">Új SQL virtuálisgép-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="160c6-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="160c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="160c6-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="160c6-105">DESCRIPTION</span></span>
<span data-ttu-id="160c6-106">Az New-AzSqlVMGroup parancsmag létrehoz egy Azure SQL Virtual Machine-csoportot.</span><span class="sxs-lookup"><span data-stu-id="160c6-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="160c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="160c6-107">EXAMPLES</span></span>

### <span data-ttu-id="160c6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="160c6-108">Example 1</span></span>
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

<span data-ttu-id="160c6-109">Új Azure SQL Virtual Machine-csoportot hoz létre, amelyben a teszt-csoport VM az erőforráscsoport ResourceGroup01 van.</span><span class="sxs-lookup"><span data-stu-id="160c6-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="160c6-110">a $profile a Microsoft. Azure. Management. SqlVirtualMachine. models. WsfcDomainProfile fájltípusú objektum.</span><span class="sxs-lookup"><span data-stu-id="160c6-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="160c6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="160c6-111">PARAMETERS</span></span>

### <span data-ttu-id="160c6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="160c6-112">-AsJob</span></span>
<span data-ttu-id="160c6-113">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="160c6-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="160c6-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="160c6-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="160c6-115">A fürtök létrehozásához használt név</span><span class="sxs-lookup"><span data-stu-id="160c6-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="160c6-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="160c6-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="160c6-117">Az üzemeltetési fürtökhöz használt név</span><span class="sxs-lookup"><span data-stu-id="160c6-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="160c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160c6-118">-DefaultProfile</span></span>
<span data-ttu-id="160c6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="160c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160c6-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="160c6-120">-DomainFqdn</span></span>
<span data-ttu-id="160c6-121">A tartomány teljesen minősített neve</span><span class="sxs-lookup"><span data-stu-id="160c6-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="160c6-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="160c6-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="160c6-123">A fájlmegosztásról választható elérési útja</span><span class="sxs-lookup"><span data-stu-id="160c6-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="160c6-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="160c6-124">-Location</span></span>
<span data-ttu-id="160c6-125">Az SQL virtuálisgép-csoport helye.</span><span class="sxs-lookup"><span data-stu-id="160c6-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="160c6-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="160c6-126">-Name</span></span>
<span data-ttu-id="160c6-127">Az SQL virtuálisgép-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="160c6-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="160c6-128">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="160c6-128">-Offer</span></span>
<span data-ttu-id="160c6-129">A virtuális SQL Machine-csoport ajánlata.</span><span class="sxs-lookup"><span data-stu-id="160c6-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="160c6-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="160c6-130">-OuPath</span></span>
<span data-ttu-id="160c6-131">Szervezeti egység elérési útvonala, amelyben a csomópontok és a klaszterek jelen lesznek</span><span class="sxs-lookup"><span data-stu-id="160c6-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="160c6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160c6-132">-ResourceGroupName</span></span>
<span data-ttu-id="160c6-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="160c6-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="160c6-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="160c6-134">-Sku</span></span>
<span data-ttu-id="160c6-135">SQL Virtual Machine Group Edition típus</span><span class="sxs-lookup"><span data-stu-id="160c6-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="160c6-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="160c6-136">-SqlServiceAccount</span></span>
<span data-ttu-id="160c6-137">A fürtben a többi SQL-szolgáltatónál futtatandó SQL-szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="160c6-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="160c6-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="160c6-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="160c6-139">A tanú-tároló fiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="160c6-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="160c6-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="160c6-140">-StorageAccountUrl</span></span>
<span data-ttu-id="160c6-141">A tanú-tároló fiók elsődleges kulcsa</span><span class="sxs-lookup"><span data-stu-id="160c6-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="160c6-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="160c6-142">-Tag</span></span>
<span data-ttu-id="160c6-143">A virtuális SQL Machine-csoporttal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="160c6-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="160c6-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="160c6-144">-Confirm</span></span>
<span data-ttu-id="160c6-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="160c6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160c6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160c6-146">-WhatIf</span></span>
<span data-ttu-id="160c6-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="160c6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160c6-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="160c6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160c6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160c6-149">CommonParameters</span></span>
<span data-ttu-id="160c6-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="160c6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160c6-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="160c6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160c6-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="160c6-152">INPUTS</span></span>

### <span data-ttu-id="160c6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="160c6-153">System.String</span></span>

## <span data-ttu-id="160c6-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="160c6-154">OUTPUTS</span></span>

### <span data-ttu-id="160c6-155">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="160c6-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="160c6-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="160c6-156">NOTES</span></span>

## <span data-ttu-id="160c6-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="160c6-157">RELATED LINKS</span></span>
