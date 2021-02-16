---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155267"
---
# <span data-ttu-id="44447-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="44447-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="44447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44447-102">SYNOPSIS</span></span>
<span data-ttu-id="44447-103">Eltávolít egy Azure AD-rendszergazdát az SQL Felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="44447-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="44447-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44447-104">SYNTAX</span></span>

### <span data-ttu-id="44447-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44447-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44447-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44447-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44447-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44447-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44447-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44447-108">DESCRIPTION</span></span>
<span data-ttu-id="44447-109">A **Remove-AzSqlInstanceActiveDirectoryAdministrator** parancsmag eltávolítja az Azure Active Directory (Azure AD) rendszergazdáját az AzureSQL Felügyelt példányhoz az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="44447-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="44447-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44447-110">EXAMPLES</span></span>

### <span data-ttu-id="44447-111">1. példa: Rendszergazda eltávolítása</span><span class="sxs-lookup"><span data-stu-id="44447-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="44447-112">Ez a parancs eltávolítja az Erőforráscsoport01 erőforráscsoporttal társított ManagedInstanceName01 nevű felügyelt példány Azure AD-rendszergazdáját.</span><span class="sxs-lookup"><span data-stu-id="44447-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="44447-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="44447-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="44447-114">Ez a parancs eltávolítja az Azure AD-rendszergazdát a felügyelt példányobjektumból.</span><span class="sxs-lookup"><span data-stu-id="44447-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="44447-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="44447-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="44447-116">Ez a parancs eltávolítja az Azure AD rendszergazdáját felügyelt példány erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="44447-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="44447-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44447-117">PARAMETERS</span></span>

### <span data-ttu-id="44447-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44447-118">-DefaultProfile</span></span>
<span data-ttu-id="44447-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44447-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44447-120">-Force</span><span class="sxs-lookup"><span data-stu-id="44447-120">-Force</span></span>
<span data-ttu-id="44447-121">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="44447-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="44447-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44447-122">-InputObject</span></span>
<span data-ttu-id="44447-123">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="44447-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="44447-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="44447-124">-InstanceName</span></span>
<span data-ttu-id="44447-125">SQL Felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="44447-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="44447-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44447-126">-PassThru</span></span>
<span data-ttu-id="44447-127">Meghatározza, hogy vissza kell-e térnie az eltávolított AD-rendszergazdának</span><span class="sxs-lookup"><span data-stu-id="44447-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="44447-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44447-128">-ResourceGroupName</span></span>
<span data-ttu-id="44447-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44447-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="44447-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44447-130">-ResourceId</span></span>
<span data-ttu-id="44447-131">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="44447-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="44447-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44447-132">-Confirm</span></span>
<span data-ttu-id="44447-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44447-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44447-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44447-134">-WhatIf</span></span>
<span data-ttu-id="44447-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44447-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44447-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44447-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44447-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44447-137">CommonParameters</span></span>
<span data-ttu-id="44447-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44447-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44447-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44447-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44447-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44447-140">INPUTS</span></span>

### <span data-ttu-id="44447-141">System.String</span><span class="sxs-lookup"><span data-stu-id="44447-141">System.String</span></span>

## <span data-ttu-id="44447-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44447-142">OUTPUTS</span></span>

### <span data-ttu-id="44447-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="44447-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="44447-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44447-144">NOTES</span></span>

## <span data-ttu-id="44447-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44447-145">RELATED LINKS</span></span>

[<span data-ttu-id="44447-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="44447-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="44447-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="44447-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
