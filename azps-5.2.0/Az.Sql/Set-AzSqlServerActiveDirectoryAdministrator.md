---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355086"
---
# <span data-ttu-id="47d21-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47d21-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="47d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d21-102">SYNOPSIS</span></span>
<span data-ttu-id="47d21-103">Azure AD-rendszergazdát hoz létre az SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="47d21-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="47d21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47d21-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47d21-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47d21-105">DESCRIPTION</span></span>
<span data-ttu-id="47d21-106">A **Set-AzSqlServerActiveDirectoryAdministrator** parancsmag az AzureSQL Server Azure Active Directory -rendszergazdáját használja a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="47d21-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="47d21-107">Egyszerre csak egy rendszergazda létesíthet.</span><span class="sxs-lookup"><span data-stu-id="47d21-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="47d21-108">Az Azure AD következő tagjait lehet SQL Server-rendszergazdaként kiépítni:</span><span class="sxs-lookup"><span data-stu-id="47d21-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="47d21-109">Az Azure AD natív tagjai</span><span class="sxs-lookup"><span data-stu-id="47d21-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="47d21-110">Az Azure AD összevont tagjai</span><span class="sxs-lookup"><span data-stu-id="47d21-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="47d21-111">Importált tagok más Azure AD-ről, akik natív vagy összevont tagok</span><span class="sxs-lookup"><span data-stu-id="47d21-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="47d21-112">A Microsoft-fiókokként létrehozott Azure AD-csoportokat ( például a Outlook.com-, Hotmail.com- vagy Live.com-tartományokat ) nem lehet rendszergazdaként támogatni.</span><span class="sxs-lookup"><span data-stu-id="47d21-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="47d21-113">Más vendégfiókok, például a Gmail.com vagy Yahoo.com tartományában található fiókok, nem támogatottak rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="47d21-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="47d21-114">Azt javasoljuk, hogy rendszergazdaként kiépítsen egy dedikált Azure AD-csoportot.</span><span class="sxs-lookup"><span data-stu-id="47d21-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="47d21-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47d21-115">EXAMPLES</span></span>

### <span data-ttu-id="47d21-116">1. példa: Rendszergazdai csoport kiépítése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="47d21-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="47d21-117">Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a Server01 nevű kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="47d21-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="47d21-118">Ez a kiszolgáló az ResourceGroup01 erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="47d21-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="47d21-119">2. példa: Rendszergazdai felhasználó kiépítése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="47d21-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="47d21-120">Ez a parancs az Azure AD-felhasználót a Server01 nevű kiszolgáló rendszergazdájának nevezi el.</span><span class="sxs-lookup"><span data-stu-id="47d21-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="47d21-121">3. példa: Rendszergazdai csoport kiépítése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="47d21-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="47d21-122">Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a Server01 nevű kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="47d21-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="47d21-123">A parancs megadja az *ObjectId paraméter azonosítóját.*</span><span class="sxs-lookup"><span data-stu-id="47d21-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="47d21-124">Ez akkor is sikeres lesz, ha a csoport megjelenítendő neve nem egyedi.</span><span class="sxs-lookup"><span data-stu-id="47d21-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="47d21-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47d21-125">PARAMETERS</span></span>

### <span data-ttu-id="47d21-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d21-126">-DefaultProfile</span></span>
<span data-ttu-id="47d21-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="47d21-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47d21-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47d21-128">-DisplayName</span></span>
<span data-ttu-id="47d21-129">Annak az Azure AD-rendszergazdának a megjelenítendő nevét adja meg, amelyről ez a parancsmag el van ásva.</span><span class="sxs-lookup"><span data-stu-id="47d21-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="47d21-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="47d21-130">-ObjectId</span></span>
<span data-ttu-id="47d21-131">Megadja annak az Azure AD-rendszergazdának az egyedi azonosítóját, amelyről ez a parancsmag rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="47d21-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="47d21-132">Ha a megjelenítendő név nem egyedi, meg kell adnia egy értéket ehhez a paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="47d21-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="47d21-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d21-133">-ResourceGroupName</span></span>
<span data-ttu-id="47d21-134">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="47d21-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="47d21-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47d21-135">-ServerName</span></span>
<span data-ttu-id="47d21-136">Annak az SQL Servernek a nevét adja meg, amelyhez a parancsmag rendszergazdai jogosultságot ad.</span><span class="sxs-lookup"><span data-stu-id="47d21-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="47d21-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47d21-137">-Confirm</span></span>
<span data-ttu-id="47d21-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="47d21-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d21-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d21-139">-WhatIf</span></span>
<span data-ttu-id="47d21-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="47d21-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47d21-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47d21-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d21-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d21-142">CommonParameters</span></span>
<span data-ttu-id="47d21-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d21-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d21-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47d21-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d21-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47d21-145">INPUTS</span></span>

### <span data-ttu-id="47d21-146">System.String</span><span class="sxs-lookup"><span data-stu-id="47d21-146">System.String</span></span>

### <span data-ttu-id="47d21-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="47d21-147">System.Guid</span></span>

## <span data-ttu-id="47d21-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d21-148">OUTPUTS</span></span>

### <span data-ttu-id="47d21-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="47d21-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="47d21-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47d21-150">NOTES</span></span>

## <span data-ttu-id="47d21-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47d21-151">RELATED LINKS</span></span>

[<span data-ttu-id="47d21-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47d21-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="47d21-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="47d21-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="47d21-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="47d21-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="47d21-155">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="47d21-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


