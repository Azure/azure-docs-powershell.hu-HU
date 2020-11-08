---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: ce700b90194e1cd0fcdf05162696ae980d24ad01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014187"
---
# <span data-ttu-id="59612-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="59612-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="59612-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59612-102">SYNOPSIS</span></span>
<span data-ttu-id="59612-103">SQL-virtuálisgép frissítése</span><span class="sxs-lookup"><span data-stu-id="59612-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="59612-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59612-104">SYNTAX</span></span>

### <span data-ttu-id="59612-105">NameParamaterList (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59612-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59612-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="59612-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59612-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="59612-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59612-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="59612-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59612-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="59612-109">DESCRIPTION</span></span>
<span data-ttu-id="59612-110">Az Update-AzSqlVM parancsmag frissíti az SQL virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="59612-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="59612-111">Példák</span><span class="sxs-lookup"><span data-stu-id="59612-111">EXAMPLES</span></span>

### <span data-ttu-id="59612-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59612-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="59612-113">Frissíti az SQL virtuális gép címkéit.</span><span class="sxs-lookup"><span data-stu-id="59612-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="59612-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59612-114">PARAMETERS</span></span>

### <span data-ttu-id="59612-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59612-115">-AsJob</span></span>
<span data-ttu-id="59612-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="59612-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="59612-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59612-117">-DefaultProfile</span></span>
<span data-ttu-id="59612-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59612-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59612-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59612-119">-InputObject</span></span>
<span data-ttu-id="59612-120">Virtuális SQL Machine-objektum.</span><span class="sxs-lookup"><span data-stu-id="59612-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59612-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="59612-121">-LicenseType</span></span>
<span data-ttu-id="59612-122">Virtuális SQL Machine-licenc típusa</span><span class="sxs-lookup"><span data-stu-id="59612-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59612-123">-Name</span></span>
<span data-ttu-id="59612-124">Az SQL virtuális gép neve</span><span class="sxs-lookup"><span data-stu-id="59612-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-125">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="59612-125">-Offer</span></span>
<span data-ttu-id="59612-126">Virtuális SQL-gép ajánlata.</span><span class="sxs-lookup"><span data-stu-id="59612-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59612-127">-ResourceGroupName</span></span>
<span data-ttu-id="59612-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="59612-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59612-129">-ResourceId</span></span>
<span data-ttu-id="59612-130">SQL virtuális gép erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="59612-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59612-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="59612-131">-Sku</span></span>
<span data-ttu-id="59612-132">SQL virtuálisgép-Kiadás típusa</span><span class="sxs-lookup"><span data-stu-id="59612-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="59612-133">-SqlManagementType</span></span>
<span data-ttu-id="59612-134">SQL virtuálisgép-kezelés típusa</span><span class="sxs-lookup"><span data-stu-id="59612-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="59612-135">-Tag</span></span>
<span data-ttu-id="59612-136">Az SQL Virtual Machine-tel társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="59612-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59612-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59612-137">-Confirm</span></span>
<span data-ttu-id="59612-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59612-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59612-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59612-139">-WhatIf</span></span>
<span data-ttu-id="59612-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59612-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59612-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59612-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59612-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59612-142">CommonParameters</span></span>
<span data-ttu-id="59612-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59612-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59612-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59612-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59612-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59612-145">INPUTS</span></span>

### <span data-ttu-id="59612-146">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="59612-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="59612-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59612-147">OUTPUTS</span></span>

### <span data-ttu-id="59612-148">Microsoft. Azure. Command. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="59612-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="59612-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59612-149">NOTES</span></span>

## <span data-ttu-id="59612-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59612-150">RELATED LINKS</span></span>
