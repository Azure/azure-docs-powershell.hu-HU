---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f801d3e36fabf0fcd0b5829ed01ad0410517a0c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497220"
---
# <span data-ttu-id="2664e-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2664e-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="2664e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2664e-102">SYNOPSIS</span></span>
<span data-ttu-id="2664e-103">Az SQL Server Azure AD-rendszergazdája.</span><span class="sxs-lookup"><span data-stu-id="2664e-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2664e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2664e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2664e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2664e-105">DESCRIPTION</span></span>
<span data-ttu-id="2664e-106">A **set-AzureRmSqlServerActiveDirectoryAdministrator** parancsmag a jelenlegi előfizetésben az Azure Active Directoryt (Azure ad) kezelőt, az AzureSQL Servert.</span><span class="sxs-lookup"><span data-stu-id="2664e-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="2664e-107">Egyszerre csak egy rendszergazda állíthat elő.</span><span class="sxs-lookup"><span data-stu-id="2664e-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="2664e-108">Az Azure AD következő tagjai kioszthatók SQL Server-rendszergazdaként:</span><span class="sxs-lookup"><span data-stu-id="2664e-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="2664e-109">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="2664e-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="2664e-110">Az Azure AD szövetséges tagjai</span><span class="sxs-lookup"><span data-stu-id="2664e-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="2664e-111">Importált tagok más Azure-hirdetésekből, akik natív vagy szövetséges tagok</span><span class="sxs-lookup"><span data-stu-id="2664e-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="2664e-112">A biztonsági csoportokba létrehozott Azure-HIRDETÉSCSOPORTOK Microsoft-fiókjai (például az Outlook.com, a Hotmail.com vagy a Live.com tartományban) nem használhatók rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="2664e-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="2664e-113">A többi vendégfiók, például a Gmail.com vagy a Yahoo.com tartománya nem támogatott rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="2664e-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="2664e-114">Azt javasoljuk, hogy rendszergazdaként hozza létre a dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="2664e-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="2664e-115">Példák</span><span class="sxs-lookup"><span data-stu-id="2664e-115">EXAMPLES</span></span>

### <span data-ttu-id="2664e-116">1. példa: rendszergazdai csoport létesítése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="2664e-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="2664e-117">Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.</span><span class="sxs-lookup"><span data-stu-id="2664e-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="2664e-118">Ez a kiszolgáló az erőforráscsoport ResourceGroup01 van társítva.</span><span class="sxs-lookup"><span data-stu-id="2664e-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="2664e-119">2. példa: rendszergazdai felhasználó létesítése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="2664e-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="2664e-120">Ez a parancs az Azure AD-felhasználót rendszergazdaként használja a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2664e-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="2664e-121">3. példa: rendszergazdai csoport létesítése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="2664e-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="2664e-122">Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.</span><span class="sxs-lookup"><span data-stu-id="2664e-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="2664e-123">A parancs a *ObjectId* paraméter azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2664e-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="2664e-124">Ez gondoskodik arról, hogy a parancs akkor is sikeres legyen, ha a csoport megjelenítendő neve nem egyedi.</span><span class="sxs-lookup"><span data-stu-id="2664e-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="2664e-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2664e-125">PARAMETERS</span></span>

### <span data-ttu-id="2664e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2664e-126">-DefaultProfile</span></span>
<span data-ttu-id="2664e-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2664e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2664e-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2664e-128">-DisplayName</span></span>
<span data-ttu-id="2664e-129">Annak az Azure AD administratornak a megjelenítendő nevét adja meg, amely a parancsmag rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="2664e-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="2664e-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2664e-130">-ObjectId</span></span>
<span data-ttu-id="2664e-131">Annak az Azure AD Administrator-nek az egyedi AZONOSÍTÓját adja meg, amely a parancsmag rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="2664e-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="2664e-132">Ha a megjelenítendő név nem egyedi, akkor ehhez a paraméterhez meg kell adnia egy értéket.</span><span class="sxs-lookup"><span data-stu-id="2664e-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2664e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2664e-133">-ResourceGroupName</span></span>
<span data-ttu-id="2664e-134">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="2664e-134">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2664e-135">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2664e-135">-ServerName</span></span>
<span data-ttu-id="2664e-136">Annak az SQL-kiszolgálónak a neve, amelyhez a parancsmag a rendszergazda rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="2664e-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2664e-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2664e-137">-Confirm</span></span>
<span data-ttu-id="2664e-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2664e-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2664e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2664e-139">-WhatIf</span></span>
<span data-ttu-id="2664e-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2664e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2664e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2664e-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2664e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2664e-142">CommonParameters</span></span>
<span data-ttu-id="2664e-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2664e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2664e-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2664e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2664e-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2664e-145">INPUTS</span></span>

### <span data-ttu-id="2664e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2664e-146">System.String</span></span>

### <span data-ttu-id="2664e-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2664e-147">System.Guid</span></span>

## <span data-ttu-id="2664e-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2664e-148">OUTPUTS</span></span>

### <span data-ttu-id="2664e-149">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="2664e-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="2664e-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2664e-150">NOTES</span></span>

## <span data-ttu-id="2664e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2664e-151">RELATED LINKS</span></span>

[<span data-ttu-id="2664e-152">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2664e-152">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="2664e-153">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2664e-153">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="2664e-154">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2664e-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


