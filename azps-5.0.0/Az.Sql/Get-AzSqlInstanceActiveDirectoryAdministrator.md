---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296639"
---
# <span data-ttu-id="a5829-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a5829-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a5829-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5829-102">SYNOPSIS</span></span>
<span data-ttu-id="a5829-103">Információt ad az SQL-alapú felügyelt példányról az Azure AD-rendszergazdákról.</span><span class="sxs-lookup"><span data-stu-id="a5829-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="a5829-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5829-104">SYNTAX</span></span>

### <span data-ttu-id="a5829-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5829-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5829-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5829-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5829-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5829-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5829-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5829-108">DESCRIPTION</span></span>
<span data-ttu-id="a5829-109">A **Get-AzSqlInstanceActiveDirectoryAdministrator** parancsmag információkat kap az Azure Active Directory (Azure ad) rendszergazdájáról egy, a jelenlegi előfizetésben AzureSQL felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="a5829-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="a5829-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5829-110">EXAMPLES</span></span>

### <span data-ttu-id="a5829-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a5829-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a5829-112">Ez a parancs információt ad az Azure AD rendszergazdájáról egy olyan, ManagedInstance01 nevű felügyelt példányról, amely a ResourceGroup01 nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="a5829-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="a5829-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a5829-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a5829-114">Ez a parancs információt ad az Azure AD rendszergazdájáról egy felügyelt objektumról.</span><span class="sxs-lookup"><span data-stu-id="a5829-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="a5829-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a5829-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a5829-116">Ez a parancs információt ad az Azure AD rendszergazdájáról a felügyelt példányok erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="a5829-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="a5829-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5829-117">PARAMETERS</span></span>

### <span data-ttu-id="a5829-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5829-118">-DefaultProfile</span></span>
<span data-ttu-id="a5829-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5829-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5829-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5829-120">-InputObject</span></span>
<span data-ttu-id="a5829-121">A használni kívánt felügyelt példány-objektum.</span><span class="sxs-lookup"><span data-stu-id="a5829-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="a5829-122">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="a5829-122">-InstanceName</span></span>
<span data-ttu-id="a5829-123">SQL-kezelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="a5829-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="a5829-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5829-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5829-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5829-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5829-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5829-126">-ResourceId</span></span>
<span data-ttu-id="a5829-127">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a5829-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="a5829-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5829-128">CommonParameters</span></span>
<span data-ttu-id="a5829-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5829-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5829-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5829-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5829-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5829-131">INPUTS</span></span>

### <span data-ttu-id="a5829-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a5829-132">System.String</span></span>

## <span data-ttu-id="a5829-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5829-133">OUTPUTS</span></span>

### <span data-ttu-id="a5829-134">Microsoft. Azure. Command. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a5829-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a5829-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5829-135">NOTES</span></span>

## <span data-ttu-id="a5829-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5829-136">RELATED LINKS</span></span>

[<span data-ttu-id="a5829-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a5829-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="a5829-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a5829-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
