---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014289"
---
# <span data-ttu-id="b7740-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7740-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b7740-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7740-102">SYNOPSIS</span></span>
<span data-ttu-id="b7740-103">Információt ad az SQL-alapú felügyelt példányról az Azure AD-rendszergazdákról.</span><span class="sxs-lookup"><span data-stu-id="b7740-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="b7740-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7740-104">SYNTAX</span></span>

### <span data-ttu-id="b7740-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7740-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7740-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7740-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7740-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7740-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7740-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7740-108">DESCRIPTION</span></span>
<span data-ttu-id="b7740-109">A **Get-AzSqlInstanceActiveDirectoryAdministrator** parancsmag információkat kap az Azure Active Directory (Azure ad) rendszergazdájáról egy, a jelenlegi előfizetésben AzureSQL felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="b7740-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="b7740-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b7740-110">EXAMPLES</span></span>

### <span data-ttu-id="b7740-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7740-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b7740-112">Ez a parancs információt ad az Azure AD rendszergazdájáról egy olyan, ManagedInstance01 nevű felügyelt példányról, amely a ResourceGroup01 nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="b7740-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="b7740-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b7740-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b7740-114">Ez a parancs információt ad az Azure AD rendszergazdájáról egy felügyelt objektumról.</span><span class="sxs-lookup"><span data-stu-id="b7740-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="b7740-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="b7740-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b7740-116">Ez a parancs információt ad az Azure AD rendszergazdájáról a felügyelt példányok erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="b7740-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="b7740-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7740-117">PARAMETERS</span></span>

### <span data-ttu-id="b7740-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7740-118">-DefaultProfile</span></span>
<span data-ttu-id="b7740-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7740-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7740-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7740-120">-InputObject</span></span>
<span data-ttu-id="b7740-121">A használni kívánt felügyelt példány-objektum.</span><span class="sxs-lookup"><span data-stu-id="b7740-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="b7740-122">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="b7740-122">-InstanceName</span></span>
<span data-ttu-id="b7740-123">SQL-kezelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="b7740-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="b7740-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7740-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7740-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7740-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7740-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7740-126">-ResourceId</span></span>
<span data-ttu-id="b7740-127">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b7740-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="b7740-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7740-128">CommonParameters</span></span>
<span data-ttu-id="b7740-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7740-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7740-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7740-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7740-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7740-131">INPUTS</span></span>

### <span data-ttu-id="b7740-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b7740-132">System.String</span></span>

## <span data-ttu-id="b7740-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7740-133">OUTPUTS</span></span>

### <span data-ttu-id="b7740-134">Microsoft. Azure. Command. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="b7740-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b7740-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7740-135">NOTES</span></span>

## <span data-ttu-id="b7740-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7740-136">RELATED LINKS</span></span>

[<span data-ttu-id="b7740-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7740-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7740-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7740-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
