---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: b29af2f5f8931876d1bf23d05072e92dc4eb588e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669016"
---
# <span data-ttu-id="45eff-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="45eff-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="45eff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45eff-102">SYNOPSIS</span></span>
<span data-ttu-id="45eff-103">Megkapja az adatbázis biztonságos kapcsolati házirendjét.</span><span class="sxs-lookup"><span data-stu-id="45eff-103">Gets the secure connection policy for a database.</span></span>

## <span data-ttu-id="45eff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45eff-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45eff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45eff-105">DESCRIPTION</span></span>
<span data-ttu-id="45eff-106">A **Get-AzSqlDatabaseSecureConnectionPolicy** parancsmag egy Azure SQL-adatbázis titkosított csatornájának házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="45eff-106">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="45eff-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="45eff-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="45eff-108">A parancsmag sikeres futtatását követően egy olyan objektumot ad eredményül, amely leírja az aktuális titkosított csatorna házirendjét, valamint az adatbázis-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="45eff-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="45eff-109">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="45eff-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="45eff-110">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="45eff-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="45eff-111">Példák</span><span class="sxs-lookup"><span data-stu-id="45eff-111">EXAMPLES</span></span>

### <span data-ttu-id="45eff-112">Példa 1: az Azure SQL-adatbázisok titkosított csatornás házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="45eff-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="45eff-113">Ez a parancs a database01 nevű Azure SQL-adatbázis titkosított csatornájának házirendjét kapja meg a kiszolgálón, a server01.</span><span class="sxs-lookup"><span data-stu-id="45eff-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="45eff-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45eff-114">PARAMETERS</span></span>

### <span data-ttu-id="45eff-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45eff-115">-DatabaseName</span></span>
<span data-ttu-id="45eff-116">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45eff-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="45eff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45eff-117">-DefaultProfile</span></span>
<span data-ttu-id="45eff-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45eff-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45eff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45eff-119">-ResourceGroupName</span></span>
<span data-ttu-id="45eff-120">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="45eff-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="45eff-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="45eff-121">-ServerName</span></span>
<span data-ttu-id="45eff-122">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45eff-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="45eff-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45eff-123">-Confirm</span></span>
<span data-ttu-id="45eff-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45eff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45eff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45eff-125">-WhatIf</span></span>
<span data-ttu-id="45eff-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45eff-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45eff-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45eff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45eff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45eff-128">CommonParameters</span></span>
<span data-ttu-id="45eff-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45eff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45eff-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45eff-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45eff-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45eff-131">INPUTS</span></span>

### <span data-ttu-id="45eff-132">System. String</span><span class="sxs-lookup"><span data-stu-id="45eff-132">System.String</span></span>

## <span data-ttu-id="45eff-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45eff-133">OUTPUTS</span></span>

### <span data-ttu-id="45eff-134">Microsoft. Azure. Command. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="45eff-134">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="45eff-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45eff-135">NOTES</span></span>

## <span data-ttu-id="45eff-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45eff-136">RELATED LINKS</span></span>
