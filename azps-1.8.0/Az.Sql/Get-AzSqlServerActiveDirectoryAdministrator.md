---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f98e362c10a0773f16ae4b687e5d725fb12f5053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668957"
---
# <span data-ttu-id="6df16-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6df16-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="6df16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6df16-102">SYNOPSIS</span></span>
<span data-ttu-id="6df16-103">Információt kap az Azure AD Administrator for SQL Serverről.</span><span class="sxs-lookup"><span data-stu-id="6df16-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="6df16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6df16-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6df16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6df16-105">DESCRIPTION</span></span>
<span data-ttu-id="6df16-106">A **Get-AzSqlServerActiveDirectoryAdministrator** parancsmag információkat kap az Azure Active Directory (Azure ad) rendszergazdájáról az aktuális előfizetéshez tartozó AzureSQL-kiszolgálókon.</span><span class="sxs-lookup"><span data-stu-id="6df16-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="6df16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6df16-107">EXAMPLES</span></span>

### <span data-ttu-id="6df16-108">1. példa: adatok beolvasása a kiszolgáló rendszergazdájával</span><span class="sxs-lookup"><span data-stu-id="6df16-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6df16-109">Ez a parancs információt ad az Azure AD rendszergazdájáról egy olyan Server01 nevű kiszolgálón, amely egy ResourceGroup01 nevű erőforráscsoport nevével van társítva.</span><span class="sxs-lookup"><span data-stu-id="6df16-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6df16-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6df16-110">PARAMETERS</span></span>

### <span data-ttu-id="6df16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df16-111">-DefaultProfile</span></span>
<span data-ttu-id="6df16-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6df16-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6df16-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df16-113">-ResourceGroupName</span></span>
<span data-ttu-id="6df16-114">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="6df16-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="6df16-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6df16-115">-ServerName</span></span>
<span data-ttu-id="6df16-116">Annak az SQL-kiszolgálónak a neve, amelyhez ez a parancsmag információkat kap.</span><span class="sxs-lookup"><span data-stu-id="6df16-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="6df16-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6df16-117">-Confirm</span></span>
<span data-ttu-id="6df16-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6df16-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df16-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df16-119">-WhatIf</span></span>
<span data-ttu-id="6df16-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6df16-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df16-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6df16-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df16-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df16-122">CommonParameters</span></span>
<span data-ttu-id="6df16-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6df16-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df16-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6df16-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df16-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df16-125">INPUTS</span></span>

### <span data-ttu-id="6df16-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6df16-126">System.String</span></span>

## <span data-ttu-id="6df16-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6df16-127">OUTPUTS</span></span>

### <span data-ttu-id="6df16-128">Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="6df16-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="6df16-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6df16-129">NOTES</span></span>

## <span data-ttu-id="6df16-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6df16-130">RELATED LINKS</span></span>

[<span data-ttu-id="6df16-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6df16-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6df16-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6df16-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6df16-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6df16-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


