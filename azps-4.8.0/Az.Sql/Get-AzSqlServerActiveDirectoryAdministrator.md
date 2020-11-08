---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181358"
---
# <span data-ttu-id="ae703-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ae703-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ae703-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae703-102">SYNOPSIS</span></span>
<span data-ttu-id="ae703-103">Információt kap az Azure AD Administrator for SQL Serverről.</span><span class="sxs-lookup"><span data-stu-id="ae703-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="ae703-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae703-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae703-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae703-105">DESCRIPTION</span></span>
<span data-ttu-id="ae703-106">A **Get-AzSqlServerActiveDirectoryAdministrator** parancsmag információkat kap az Azure Active Directory (Azure ad) rendszergazdájáról az aktuális előfizetéshez tartozó AzureSQL-kiszolgálókon.</span><span class="sxs-lookup"><span data-stu-id="ae703-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ae703-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae703-107">EXAMPLES</span></span>

### <span data-ttu-id="ae703-108">1. példa: adatok beolvasása a kiszolgáló rendszergazdájával</span><span class="sxs-lookup"><span data-stu-id="ae703-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="ae703-109">Ez a parancs információt ad az Azure AD rendszergazdájáról egy olyan Server01 nevű kiszolgálón, amely egy ResourceGroup01 nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="ae703-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ae703-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae703-110">PARAMETERS</span></span>

### <span data-ttu-id="ae703-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae703-111">-DefaultProfile</span></span>
<span data-ttu-id="ae703-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae703-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae703-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae703-113">-ResourceGroupName</span></span>
<span data-ttu-id="ae703-114">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ae703-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="ae703-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ae703-115">-ServerName</span></span>
<span data-ttu-id="ae703-116">Annak az SQL-kiszolgálónak a neve, amelyhez ez a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="ae703-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="ae703-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae703-117">-Confirm</span></span>
<span data-ttu-id="ae703-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae703-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae703-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae703-119">-WhatIf</span></span>
<span data-ttu-id="ae703-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae703-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae703-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae703-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae703-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae703-122">CommonParameters</span></span>
<span data-ttu-id="ae703-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae703-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae703-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae703-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae703-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae703-125">INPUTS</span></span>

### <span data-ttu-id="ae703-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ae703-126">System.String</span></span>

## <span data-ttu-id="ae703-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae703-127">OUTPUTS</span></span>

### <span data-ttu-id="ae703-128">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="ae703-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ae703-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae703-129">NOTES</span></span>

## <span data-ttu-id="ae703-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae703-130">RELATED LINKS</span></span>

[<span data-ttu-id="ae703-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ae703-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ae703-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ae703-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ae703-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ae703-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ae703-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ae703-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


