---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499127"
---
# <span data-ttu-id="027d9-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="027d9-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="027d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="027d9-102">SYNOPSIS</span></span>
<span data-ttu-id="027d9-103">Az SQL Server Azure AD-rendszergazdája.</span><span class="sxs-lookup"><span data-stu-id="027d9-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="027d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="027d9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="027d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="027d9-105">DESCRIPTION</span></span>
<span data-ttu-id="027d9-106">A **set-AzureRmSqlServerActiveDirectoryAdministrator** parancsmag a jelenlegi előfizetésben az Azure Active Directoryt (Azure ad) kezelőt, az AzureSQL Servert.</span><span class="sxs-lookup"><span data-stu-id="027d9-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="027d9-107">Egyszerre csak egy rendszergazda állíthat elő.</span><span class="sxs-lookup"><span data-stu-id="027d9-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="027d9-108">Az Azure AD következő tagjai kioszthatók SQL Server-rendszergazdaként:</span><span class="sxs-lookup"><span data-stu-id="027d9-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="027d9-109">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="027d9-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="027d9-110">Az Azure AD szövetséges tagjai</span><span class="sxs-lookup"><span data-stu-id="027d9-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="027d9-111">Importált tagok más Azure-hirdetésekből, akik natív vagy szövetséges tagok</span><span class="sxs-lookup"><span data-stu-id="027d9-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="027d9-112">Biztonsági csoportként létrehozott Azure AD-csoportok</span><span class="sxs-lookup"><span data-stu-id="027d9-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="027d9-113">A Microsoft-fiókok, például a Outlook.com, a Hotmail.com vagy a Live.com tartományok nem támogatottak rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="027d9-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="027d9-114">A többi vendégfiók, például a Gmail.com vagy a Yahoo.com tartománya nem támogatott rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="027d9-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="027d9-115">Azt javasoljuk, hogy rendszergazdaként hozza létre a dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="027d9-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="027d9-116">Példák</span><span class="sxs-lookup"><span data-stu-id="027d9-116">EXAMPLES</span></span>

### <span data-ttu-id="027d9-117">1. példa: rendszergazdai csoport létesítése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="027d9-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="027d9-118">Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.</span><span class="sxs-lookup"><span data-stu-id="027d9-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="027d9-119">Ez a kiszolgáló az erőforráscsoport ResourceGroup01 van társítva.</span><span class="sxs-lookup"><span data-stu-id="027d9-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="027d9-120">2. példa: rendszergazdai felhasználó létesítése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="027d9-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="027d9-121">Ez a parancs az Azure AD-felhasználót rendszergazdaként használja a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="027d9-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="027d9-122">3. példa: rendszergazdai csoport létesítése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="027d9-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="027d9-123">Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.</span><span class="sxs-lookup"><span data-stu-id="027d9-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="027d9-124">A parancs a *ObjectId* paraméter azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="027d9-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="027d9-125">Ez gondoskodik arról, hogy a parancs akkor is sikeres legyen, ha a csoport megjelenítendő neve nem egyedi.</span><span class="sxs-lookup"><span data-stu-id="027d9-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="027d9-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="027d9-126">PARAMETERS</span></span>

### <span data-ttu-id="027d9-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="027d9-127">-DisplayName</span></span>
<span data-ttu-id="027d9-128">Annak az Azure AD administratornak a megjelenítendő nevét adja meg, amely a parancsmag rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="027d9-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="027d9-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="027d9-129">-ObjectId</span></span>
<span data-ttu-id="027d9-130">Annak az Azure AD Administrator-nek az egyedi AZONOSÍTÓját adja meg, amely a parancsmag rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="027d9-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="027d9-131">Ha a megjelenítendő név nem egyedi, akkor ehhez a paraméterhez meg kell adnia egy értéket.</span><span class="sxs-lookup"><span data-stu-id="027d9-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="027d9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027d9-132">-ResourceGroupName</span></span>
<span data-ttu-id="027d9-133">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="027d9-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="027d9-134">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="027d9-134">-ServerName</span></span>
<span data-ttu-id="027d9-135">Annak az SQL-kiszolgálónak a neve, amelyhez a parancsmag a rendszergazda rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="027d9-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="027d9-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="027d9-136">-Confirm</span></span>
<span data-ttu-id="027d9-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="027d9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="027d9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="027d9-138">-WhatIf</span></span>
<span data-ttu-id="027d9-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="027d9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="027d9-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="027d9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="027d9-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027d9-141">-DefaultProfile</span></span>
<span data-ttu-id="027d9-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="027d9-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="027d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027d9-143">CommonParameters</span></span>
<span data-ttu-id="027d9-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="027d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027d9-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027d9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027d9-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="027d9-146">INPUTS</span></span>

## <span data-ttu-id="027d9-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="027d9-147">OUTPUTS</span></span>

### <span data-ttu-id="027d9-148">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="027d9-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="027d9-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="027d9-149">NOTES</span></span>

## <span data-ttu-id="027d9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="027d9-150">RELATED LINKS</span></span>

[<span data-ttu-id="027d9-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="027d9-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="027d9-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="027d9-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="027d9-153">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="027d9-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


