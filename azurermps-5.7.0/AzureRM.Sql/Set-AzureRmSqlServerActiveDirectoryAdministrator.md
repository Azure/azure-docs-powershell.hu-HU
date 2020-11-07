---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 43dbbe6ca4f24e98bcfc45703c387ccb5fb4db03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672508"
---
# <span data-ttu-id="e8da3-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8da3-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e8da3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8da3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8da3-103">Az SQL Server Azure AD-rendszergazdája.</span><span class="sxs-lookup"><span data-stu-id="e8da3-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8da3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8da3-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8da3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8da3-105">DESCRIPTION</span></span>
<span data-ttu-id="e8da3-106">A **set-AzureRmSqlServerActiveDirectoryAdministrator** parancsmag a jelenlegi előfizetésben az Azure Active Directoryt (Azure ad) kezelőt, az AzureSQL Servert.</span><span class="sxs-lookup"><span data-stu-id="e8da3-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="e8da3-107">Egyszerre csak egy rendszergazda állíthat elő.</span><span class="sxs-lookup"><span data-stu-id="e8da3-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="e8da3-108">Az Azure AD következő tagjai kioszthatók SQL Server-rendszergazdaként:</span><span class="sxs-lookup"><span data-stu-id="e8da3-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="e8da3-109">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="e8da3-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="e8da3-110">Az Azure AD szövetséges tagjai</span><span class="sxs-lookup"><span data-stu-id="e8da3-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="e8da3-111">Importált tagok más Azure-hirdetésekből, akik natív vagy szövetséges tagok</span><span class="sxs-lookup"><span data-stu-id="e8da3-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="e8da3-112">Biztonsági csoportként létrehozott Azure AD-csoportok</span><span class="sxs-lookup"><span data-stu-id="e8da3-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="e8da3-113">A Microsoft-fiókok, például a Outlook.com, a Hotmail.com vagy a Live.com tartományok nem támogatottak rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="e8da3-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e8da3-114">A többi vendégfiók, például a Gmail.com vagy a Yahoo.com tartománya nem támogatott rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="e8da3-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="e8da3-115">Azt javasoljuk, hogy rendszergazdaként hozza létre a dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="e8da3-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="e8da3-116">Példák</span><span class="sxs-lookup"><span data-stu-id="e8da3-116">EXAMPLES</span></span>

### <span data-ttu-id="e8da3-117">1. példa: rendszergazdai csoport létesítése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="e8da3-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e8da3-118">Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.</span><span class="sxs-lookup"><span data-stu-id="e8da3-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="e8da3-119">Ez a kiszolgáló az erőforráscsoport ResourceGroup01 van társítva.</span><span class="sxs-lookup"><span data-stu-id="e8da3-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e8da3-120">2. példa: rendszergazdai felhasználó létesítése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="e8da3-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e8da3-121">Ez a parancs az Azure AD-felhasználót rendszergazdaként használja a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e8da3-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="e8da3-122">3. példa: rendszergazdai csoport létesítése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="e8da3-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e8da3-123">Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.</span><span class="sxs-lookup"><span data-stu-id="e8da3-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="e8da3-124">A parancs a *ObjectId* paraméter azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8da3-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="e8da3-125">Ez gondoskodik arról, hogy a parancs akkor is sikeres legyen, ha a csoport megjelenítendő neve nem egyedi.</span><span class="sxs-lookup"><span data-stu-id="e8da3-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="e8da3-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8da3-126">PARAMETERS</span></span>

### <span data-ttu-id="e8da3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8da3-127">-DefaultProfile</span></span>
<span data-ttu-id="e8da3-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e8da3-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8da3-129">-DisplayName</span></span>
<span data-ttu-id="e8da3-130">Annak az Azure AD administratornak a megjelenítendő nevét adja meg, amely a parancsmag rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="e8da3-130">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e8da3-131">-ObjectId</span></span>
<span data-ttu-id="e8da3-132">Annak az Azure AD Administrator-nek az egyedi AZONOSÍTÓját adja meg, amely a parancsmag rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="e8da3-132">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="e8da3-133">Ha a megjelenítendő név nem egyedi, akkor ehhez a paraméterhez meg kell adnia egy értéket.</span><span class="sxs-lookup"><span data-stu-id="e8da3-133">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8da3-134">-ResourceGroupName</span></span>
<span data-ttu-id="e8da3-135">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="e8da3-135">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-136">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e8da3-136">-ServerName</span></span>
<span data-ttu-id="e8da3-137">Annak az SQL-kiszolgálónak a neve, amelyhez a parancsmag a rendszergazda rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="e8da3-137">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8da3-138">-Confirm</span></span>
<span data-ttu-id="e8da3-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8da3-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8da3-140">-WhatIf</span></span>
<span data-ttu-id="e8da3-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8da3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8da3-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8da3-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8da3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8da3-143">CommonParameters</span></span>
<span data-ttu-id="e8da3-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8da3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8da3-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8da3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8da3-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8da3-146">INPUTS</span></span>

### <span data-ttu-id="e8da3-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="e8da3-147">None</span></span>
<span data-ttu-id="e8da3-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e8da3-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8da3-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8da3-149">OUTPUTS</span></span>

### <span data-ttu-id="e8da3-150">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e8da3-150">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e8da3-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8da3-151">NOTES</span></span>

## <span data-ttu-id="e8da3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8da3-152">RELATED LINKS</span></span>

[<span data-ttu-id="e8da3-153">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8da3-153">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e8da3-154">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8da3-154">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="e8da3-155">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e8da3-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


