---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181293"
---
# <span data-ttu-id="a54ee-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a54ee-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a54ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a54ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a54ee-103">Kiépít egy Azure AD-rendszergazdát az SQL-alapú felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="a54ee-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="a54ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a54ee-104">SYNTAX</span></span>

### <span data-ttu-id="a54ee-105">UseResourceGroupAndInstanceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a54ee-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a54ee-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a54ee-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a54ee-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a54ee-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a54ee-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a54ee-108">DESCRIPTION</span></span>
<span data-ttu-id="a54ee-109">A **set-AzSqlInstanceActiveDirectoryAdministrator** parancsmag a jelenlegi előfizetésben az Azure Active Directory (Azure AD-ad) AzureSQL felügyelt példányára vonatkozó rendelkezéseket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="a54ee-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="a54ee-110">Egyszerre csak egy rendszergazda állíthat elő.</span><span class="sxs-lookup"><span data-stu-id="a54ee-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="a54ee-111">Az Azure AD következő tagjai kioszthatók SQL felügyelt példány-rendszergazdaként:</span><span class="sxs-lookup"><span data-stu-id="a54ee-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="a54ee-112">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="a54ee-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="a54ee-113">Az Azure AD szövetséges tagjai</span><span class="sxs-lookup"><span data-stu-id="a54ee-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="a54ee-114">A biztonsági csoportokként létrehozott Azure-HIRDETÉSCSOPORTOK a más Azure-hirdetésekből importált tagokat nem támogatják rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="a54ee-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="a54ee-115">A Microsoft-fiókok, például a Outlook.com, a Hotmail.com vagy a Live.com tartományok nem támogatottak rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="a54ee-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a54ee-116">A többi vendégfiók, például a Gmail.com vagy a Yahoo.com tartománya nem támogatott rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="a54ee-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a54ee-117">Azt javasoljuk, hogy rendszergazdaként hozza létre a dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="a54ee-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="a54ee-118">Példák</span><span class="sxs-lookup"><span data-stu-id="a54ee-118">EXAMPLES</span></span>

### <span data-ttu-id="a54ee-119">Példa 1: rendszergazdai csoport létesítése az erőforráscsoport által társított felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="a54ee-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a54ee-120">Ez a parancs a DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat a ManagedInstance01 nevű felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="a54ee-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="a54ee-121">Ez a kiszolgáló az erőforráscsoport ResourceGroup01 van társítva.</span><span class="sxs-lookup"><span data-stu-id="a54ee-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a54ee-122">2. példa: rendszergazdai felhasználó létesítése a Managed instance objektummal</span><span class="sxs-lookup"><span data-stu-id="a54ee-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="a54ee-123">Ez a parancs az Azure AD-felhasználót rendszergazdaként kezeli a Managed instance objektumból.</span><span class="sxs-lookup"><span data-stu-id="a54ee-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="a54ee-124">3. példa: rendszergazda létesítése felügyelt kiszolgálópéldány erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a54ee-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="a54ee-125">Ez a parancs az Azure AD-felhasználót rendszergazdaként kezeli a felügyelt példányok erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="a54ee-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="a54ee-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a54ee-126">PARAMETERS</span></span>

### <span data-ttu-id="a54ee-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54ee-127">-DefaultProfile</span></span>
<span data-ttu-id="a54ee-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a54ee-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54ee-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a54ee-129">-DisplayName</span></span>
<span data-ttu-id="a54ee-130">Annak a felhasználónak vagy csoportnak a megjelenítendő nevét adja meg, akinek az engedélyeit meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="a54ee-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="a54ee-131">Ennek a megjelenítendő névnek a jelenlegi előfizetéshez társított Active Directoryban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a54ee-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="a54ee-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a54ee-132">-InputObject</span></span>
<span data-ttu-id="a54ee-133">A használni kívánt felügyelt példány-objektum.</span><span class="sxs-lookup"><span data-stu-id="a54ee-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="a54ee-134">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="a54ee-134">-InstanceName</span></span>
<span data-ttu-id="a54ee-135">SQL-kezelt példány neve.</span><span class="sxs-lookup"><span data-stu-id="a54ee-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="a54ee-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a54ee-136">-ObjectId</span></span>
<span data-ttu-id="a54ee-137">Annak az Azure Active Directoryban a felhasználó vagy csoport objektum-AZONOSÍTÓját adja meg, amelynek az engedélyeit meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="a54ee-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="a54ee-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54ee-138">-ResourceGroupName</span></span>
<span data-ttu-id="a54ee-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a54ee-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="a54ee-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a54ee-140">-ResourceId</span></span>
<span data-ttu-id="a54ee-141">A használni kívánt példa erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a54ee-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="a54ee-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a54ee-142">-Confirm</span></span>
<span data-ttu-id="a54ee-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a54ee-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a54ee-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a54ee-144">-WhatIf</span></span>
<span data-ttu-id="a54ee-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a54ee-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a54ee-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a54ee-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a54ee-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54ee-147">CommonParameters</span></span>
<span data-ttu-id="a54ee-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a54ee-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54ee-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a54ee-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54ee-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a54ee-150">INPUTS</span></span>

### <span data-ttu-id="a54ee-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a54ee-151">System.String</span></span>

### <span data-ttu-id="a54ee-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a54ee-152">System.Guid</span></span>

## <span data-ttu-id="a54ee-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a54ee-153">OUTPUTS</span></span>

### <span data-ttu-id="a54ee-154">Microsoft. Azure. Command. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a54ee-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a54ee-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a54ee-155">NOTES</span></span>

## <span data-ttu-id="a54ee-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a54ee-156">RELATED LINKS</span></span>

[<span data-ttu-id="a54ee-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a54ee-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="a54ee-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a54ee-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
