---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350106"
---
# <span data-ttu-id="68447-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="68447-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="68447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68447-102">SYNOPSIS</span></span>
<span data-ttu-id="68447-103">Információkat kap az SQL Serverhez szükséges Azure AD-rendszergazdáról.</span><span class="sxs-lookup"><span data-stu-id="68447-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="68447-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="68447-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68447-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="68447-105">DESCRIPTION</span></span>
<span data-ttu-id="68447-106">A **Get-AzSqlServerActiveDirectoryAdministrator** parancsmag az aktuális előfizetésben lévő AzureSQL-kiszolgáló Azure Active Directory (Azure AD) rendszergazdájával kapcsolatos információkat kap.</span><span class="sxs-lookup"><span data-stu-id="68447-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="68447-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="68447-107">EXAMPLES</span></span>

### <span data-ttu-id="68447-108">1. példa: Információt kap egy kiszolgáló rendszergazdájától</span><span class="sxs-lookup"><span data-stu-id="68447-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="68447-109">Ez a parancs információkat kap egy Server01 nevű kiszolgáló Azure AD-rendszergazdájával kapcsolatban, amely egy ResourceGroup01 nevű erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="68447-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="68447-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68447-110">PARAMETERS</span></span>

### <span data-ttu-id="68447-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68447-111">-DefaultProfile</span></span>
<span data-ttu-id="68447-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="68447-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68447-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68447-113">-ResourceGroupName</span></span>
<span data-ttu-id="68447-114">Annak az erőforráscsoportnak a neve, amelyhez az SQL Server hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="68447-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="68447-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68447-115">-ServerName</span></span>
<span data-ttu-id="68447-116">Annak az SQL Servernek a nevét adja meg, amelyről a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="68447-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="68447-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68447-117">-Confirm</span></span>
<span data-ttu-id="68447-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="68447-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68447-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68447-119">-WhatIf</span></span>
<span data-ttu-id="68447-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="68447-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68447-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68447-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68447-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68447-122">CommonParameters</span></span>
<span data-ttu-id="68447-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68447-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68447-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68447-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68447-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68447-125">INPUTS</span></span>

### <span data-ttu-id="68447-126">System.String</span><span class="sxs-lookup"><span data-stu-id="68447-126">System.String</span></span>

## <span data-ttu-id="68447-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68447-127">OUTPUTS</span></span>

### <span data-ttu-id="68447-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="68447-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="68447-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="68447-129">NOTES</span></span>

## <span data-ttu-id="68447-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68447-130">RELATED LINKS</span></span>

[<span data-ttu-id="68447-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="68447-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="68447-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="68447-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="68447-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="68447-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="68447-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="68447-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


