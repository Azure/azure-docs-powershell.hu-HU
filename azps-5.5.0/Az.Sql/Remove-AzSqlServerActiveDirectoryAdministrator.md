---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165738"
---
# <span data-ttu-id="a2b8b-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a2b8b-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a2b8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b8b-103">Eltávolít egy Azure AD-rendszergazdát az SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a2b8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2b8b-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b8b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b8b-106">A **Remove-AzSqlServerActiveDirectoryAdministrator** parancsmag eltávolítja az AzureSql Server Azure Active Directory -rendszergazdáját a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="a2b8b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2b8b-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b8b-108">1. példa: Rendszergazda eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a2b8b-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a2b8b-109">Ez a parancs eltávolítja az Erőforráscsoport01 erőforráscsoporttal társított Kiszolgáló01 nevű kiszolgáló Azure AD-rendszergazdáját.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a2b8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2b8b-110">PARAMETERS</span></span>

### <span data-ttu-id="a2b8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b8b-111">-DefaultProfile</span></span>
<span data-ttu-id="a2b8b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2b8b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2b8b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a2b8b-113">-Force</span></span>
<span data-ttu-id="a2b8b-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2b8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="a2b8b-116">Annak az erőforráscsoportnak a neve, amelyhez az SQL Server hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="a2b8b-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2b8b-117">-ServerName</span></span>
<span data-ttu-id="a2b8b-118">Annak az SQL Servernek a nevét adja meg, amelyből a parancsmag eltávolítja a rendszergazdát.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="a2b8b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2b8b-119">-Confirm</span></span>
<span data-ttu-id="a2b8b-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b8b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b8b-121">-WhatIf</span></span>
<span data-ttu-id="a2b8b-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b8b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b8b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b8b-124">CommonParameters</span></span>
<span data-ttu-id="a2b8b-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b8b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b8b-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2b8b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b8b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2b8b-127">INPUTS</span></span>

### <span data-ttu-id="a2b8b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a2b8b-128">System.String</span></span>

## <span data-ttu-id="a2b8b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2b8b-129">OUTPUTS</span></span>

### <span data-ttu-id="a2b8b-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a2b8b-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a2b8b-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2b8b-131">NOTES</span></span>

## <span data-ttu-id="a2b8b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2b8b-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2b8b-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a2b8b-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a2b8b-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a2b8b-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a2b8b-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a2b8b-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


