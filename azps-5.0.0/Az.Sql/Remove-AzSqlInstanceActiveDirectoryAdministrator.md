---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194515"
---
# <span data-ttu-id="26c41-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="26c41-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="26c41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26c41-102">SYNOPSIS</span></span>
<span data-ttu-id="26c41-103">Eltávolítja az Azure AD administratort az SQL-alapú felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="26c41-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="26c41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26c41-104">SYNTAX</span></span>

### <span data-ttu-id="26c41-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26c41-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c41-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26c41-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26c41-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26c41-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c41-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="26c41-108">DESCRIPTION</span></span>
<span data-ttu-id="26c41-109">A **Remove-AzSqlInstanceActiveDirectoryAdministrator** parancsmag eltávolítja az Azure Active Directoryt (Azure ad) a AzureSQL felügyelt példányának a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="26c41-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="26c41-110">Példák</span><span class="sxs-lookup"><span data-stu-id="26c41-110">EXAMPLES</span></span>

### <span data-ttu-id="26c41-111">1. példa: rendszergazda eltávolítása</span><span class="sxs-lookup"><span data-stu-id="26c41-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="26c41-112">Ez a parancs eltávolítja az Azure AD administratort az erőforráscsoport ResourceGroup01 társított ManagedInstanceName01 nevű felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="26c41-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="26c41-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="26c41-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="26c41-114">Ez a parancs eltávolítja az Azure AD administratort a Managed instance objektumból.</span><span class="sxs-lookup"><span data-stu-id="26c41-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="26c41-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="26c41-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="26c41-116">Ez a parancs eltávolítja az Azure AD administratort a felügyelt példányok erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="26c41-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="26c41-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26c41-117">PARAMETERS</span></span>

### <span data-ttu-id="26c41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c41-118">-DefaultProfile</span></span>
<span data-ttu-id="26c41-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26c41-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c41-120">-Force</span><span class="sxs-lookup"><span data-stu-id="26c41-120">-Force</span></span>
<span data-ttu-id="26c41-121">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="26c41-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="26c41-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26c41-122">-InputObject</span></span>
<span data-ttu-id="26c41-123">A használni kívánt felügyelt példány-objektum.</span><span class="sxs-lookup"><span data-stu-id="26c41-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="26c41-124">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="26c41-124">-InstanceName</span></span>
<span data-ttu-id="26c41-125">SQL-kezelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="26c41-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="26c41-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26c41-126">-PassThru</span></span>
<span data-ttu-id="26c41-127">Annak megadása, hogy az eltávolított AD-rendszergazda visszaadja-e</span><span class="sxs-lookup"><span data-stu-id="26c41-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="26c41-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c41-128">-ResourceGroupName</span></span>
<span data-ttu-id="26c41-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26c41-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="26c41-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26c41-130">-ResourceId</span></span>
<span data-ttu-id="26c41-131">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="26c41-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="26c41-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26c41-132">-Confirm</span></span>
<span data-ttu-id="26c41-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26c41-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c41-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c41-134">-WhatIf</span></span>
<span data-ttu-id="26c41-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26c41-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c41-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26c41-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c41-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c41-137">CommonParameters</span></span>
<span data-ttu-id="26c41-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26c41-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c41-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26c41-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c41-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26c41-140">INPUTS</span></span>

### <span data-ttu-id="26c41-141">System. String</span><span class="sxs-lookup"><span data-stu-id="26c41-141">System.String</span></span>

## <span data-ttu-id="26c41-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26c41-142">OUTPUTS</span></span>

### <span data-ttu-id="26c41-143">Microsoft. Azure. Command. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="26c41-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="26c41-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26c41-144">NOTES</span></span>

## <span data-ttu-id="26c41-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26c41-145">RELATED LINKS</span></span>

[<span data-ttu-id="26c41-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="26c41-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="26c41-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="26c41-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
