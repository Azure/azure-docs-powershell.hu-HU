---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158307"
---
# <span data-ttu-id="e2942-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e2942-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e2942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2942-102">SYNOPSIS</span></span>
<span data-ttu-id="e2942-103">Információkat kap az SQL Felügyelt példány Azure AD-rendszergazdájának adatairól.</span><span class="sxs-lookup"><span data-stu-id="e2942-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="e2942-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2942-104">SYNTAX</span></span>

### <span data-ttu-id="e2942-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2942-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2942-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2942-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2942-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2942-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2942-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2942-108">DESCRIPTION</span></span>
<span data-ttu-id="e2942-109">A **Get-AzSqlInstanceActiveDirectoryAdministrator** parancsmag információt kap az aktuális előfizetésben lévő AzureSQL Felügyelt példány Azure Active Directory (Azure AD) rendszergazdáiról.</span><span class="sxs-lookup"><span data-stu-id="e2942-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="e2942-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2942-110">EXAMPLES</span></span>

### <span data-ttu-id="e2942-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2942-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e2942-112">Ez a parancs információt kap egy Azure AD-rendszergazdáról egy ManagedInstance01 nevű felügyelt példányról, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="e2942-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="e2942-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e2942-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e2942-114">Ez a parancs felügyelt példányobjektumból információkat kap az Azure AD-rendszergazdáról.</span><span class="sxs-lookup"><span data-stu-id="e2942-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="e2942-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e2942-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e2942-116">Ez a parancs felügyeltpéldány-erőforrás-azonosító használatával információkat kap az Azure AD rendszergazdáiról.</span><span class="sxs-lookup"><span data-stu-id="e2942-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="e2942-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2942-117">PARAMETERS</span></span>

### <span data-ttu-id="e2942-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2942-118">-DefaultProfile</span></span>
<span data-ttu-id="e2942-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2942-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2942-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2942-120">-InputObject</span></span>
<span data-ttu-id="e2942-121">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="e2942-121">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2942-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e2942-122">-InstanceName</span></span>
<span data-ttu-id="e2942-123">SQL Felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="e2942-123">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2942-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2942-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2942-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2942-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2942-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2942-126">-ResourceId</span></span>
<span data-ttu-id="e2942-127">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e2942-127">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2942-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2942-128">CommonParameters</span></span>
<span data-ttu-id="e2942-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2942-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2942-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2942-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2942-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2942-131">INPUTS</span></span>

### <span data-ttu-id="e2942-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e2942-132">System.String</span></span>

## <span data-ttu-id="e2942-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2942-133">OUTPUTS</span></span>

### <span data-ttu-id="e2942-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e2942-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e2942-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2942-135">NOTES</span></span>

## <span data-ttu-id="e2942-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2942-136">RELATED LINKS</span></span>

[<span data-ttu-id="e2942-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e2942-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e2942-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e2942-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
