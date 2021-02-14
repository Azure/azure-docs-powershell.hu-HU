---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163179"
---
# <span data-ttu-id="94e08-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94e08-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="94e08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e08-102">SYNOPSIS</span></span>
<span data-ttu-id="94e08-103">Azure AD-rendszergazdát hoz létre az SQL Felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="94e08-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="94e08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94e08-104">SYNTAX</span></span>

### <span data-ttu-id="94e08-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94e08-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e08-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e08-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94e08-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94e08-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e08-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94e08-108">DESCRIPTION</span></span>
<span data-ttu-id="94e08-109">A **Set-AzSqlInstanceActiveDirectoryAdministrator** parancsmag azure Active Directory (Azure AD) rendszergazdát hoz létre az AzureSQL Felügyelt példányhoz az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="94e08-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="94e08-110">Egyszerre csak egy rendszergazda létesíthet.</span><span class="sxs-lookup"><span data-stu-id="94e08-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="94e08-111">Az Azure AD következő tagjai sql felügyeltpéldány-rendszergazdaként is kiépítve használhatja őket:</span><span class="sxs-lookup"><span data-stu-id="94e08-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="94e08-112">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="94e08-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="94e08-113">Az Azure AD összevont tagjai</span><span class="sxs-lookup"><span data-stu-id="94e08-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="94e08-114">A más Azure AD-ről importált tagok biztonsági csoportokként létrehozott Azure AD-csoportjait nem lehet rendszergazdaként támogatni.</span><span class="sxs-lookup"><span data-stu-id="94e08-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="94e08-115">A Microsoft-fiókokat ( például a Outlook.com, a Hotmail.com és a Live.com tartományában – nem lehet rendszergazdaként támogatni.</span><span class="sxs-lookup"><span data-stu-id="94e08-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="94e08-116">Más vendégfiókok, például a Gmail.com vagy Yahoo.com tartományában található fiókok, nem támogatottak rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="94e08-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="94e08-117">Azt javasoljuk, hogy rendszergazdaként kiépítsen egy dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="94e08-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="94e08-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94e08-118">EXAMPLES</span></span>

### <span data-ttu-id="94e08-119">1. példa: Rendszergazdai csoport kiépítése az erőforráscsoporttal társított felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="94e08-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="94e08-120">Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a ManagedInstance01 nevű felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="94e08-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="94e08-121">Ez a kiszolgáló az ResourceGroup01 erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="94e08-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="94e08-122">2. példa: Rendszergazdai felhasználó kiépítése felügyelt példányobjektum használatával</span><span class="sxs-lookup"><span data-stu-id="94e08-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="94e08-123">Ez a parancs kihoz egy Azure AD-felhasználót rendszergazdaként a felügyelt példányobjektumból.</span><span class="sxs-lookup"><span data-stu-id="94e08-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="94e08-124">3. példa: Rendszergazda kiépítése felügyelt példány erőforrás-azonosítójával</span><span class="sxs-lookup"><span data-stu-id="94e08-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="94e08-125">Ez a parancs felügyelt példány erőforrás-azonosítót használó rendszergazdaként kialkossa az Azure AD-felhasználót.</span><span class="sxs-lookup"><span data-stu-id="94e08-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="94e08-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94e08-126">PARAMETERS</span></span>

### <span data-ttu-id="94e08-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e08-127">-DefaultProfile</span></span>
<span data-ttu-id="94e08-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94e08-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e08-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="94e08-129">-DisplayName</span></span>
<span data-ttu-id="94e08-130">Annak a felhasználónak vagy csoportnak a megjelenítendő nevét adja meg, akinek engedélyt kell kiadó felhasználó vagy csoport.</span><span class="sxs-lookup"><span data-stu-id="94e08-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="94e08-131">Ennek a megjelenítendő névnek az aktuális előfizetéshez társított Active Directoryban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="94e08-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e08-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e08-132">-InputObject</span></span>
<span data-ttu-id="94e08-133">A használni használt felügyeltpéldány-objektum.</span><span class="sxs-lookup"><span data-stu-id="94e08-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="94e08-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="94e08-134">-InstanceName</span></span>
<span data-ttu-id="94e08-135">SQL Felügyelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="94e08-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="94e08-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="94e08-136">-ObjectId</span></span>
<span data-ttu-id="94e08-137">Annak a felhasználónak vagy csoportnak az objektumazonosítóját adja meg az Azure Active Directoryban, amelynek engedélyeket ad meg.</span><span class="sxs-lookup"><span data-stu-id="94e08-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e08-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e08-138">-ResourceGroupName</span></span>
<span data-ttu-id="94e08-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94e08-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="94e08-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94e08-140">-ResourceId</span></span>
<span data-ttu-id="94e08-141">A használni használt példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="94e08-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="94e08-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94e08-142">-Confirm</span></span>
<span data-ttu-id="94e08-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94e08-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e08-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e08-144">-WhatIf</span></span>
<span data-ttu-id="94e08-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94e08-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e08-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94e08-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e08-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e08-147">CommonParameters</span></span>
<span data-ttu-id="94e08-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e08-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e08-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94e08-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e08-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94e08-150">INPUTS</span></span>

### <span data-ttu-id="94e08-151">System.String</span><span class="sxs-lookup"><span data-stu-id="94e08-151">System.String</span></span>

### <span data-ttu-id="94e08-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="94e08-152">System.Guid</span></span>

## <span data-ttu-id="94e08-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94e08-153">OUTPUTS</span></span>

### <span data-ttu-id="94e08-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="94e08-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="94e08-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94e08-155">NOTES</span></span>

## <span data-ttu-id="94e08-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94e08-156">RELATED LINKS</span></span>

[<span data-ttu-id="94e08-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94e08-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="94e08-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94e08-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
