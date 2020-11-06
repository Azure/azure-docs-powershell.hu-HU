---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 51e2c480b9a374136f2b040b8884cf85949b5fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498772"
---
# <span data-ttu-id="01800-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="01800-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="01800-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01800-102">SYNOPSIS</span></span>
<span data-ttu-id="01800-103">Megkapja az adatbázis biztonságos kapcsolati házirendjét.</span><span class="sxs-lookup"><span data-stu-id="01800-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01800-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01800-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01800-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01800-105">DESCRIPTION</span></span>
<span data-ttu-id="01800-106">A **Get-AzureRmSqlDatabaseSecureConnectionPolicy** parancsmag egy Azure SQL-adatbázis titkosított csatornájának házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="01800-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="01800-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="01800-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="01800-108">A parancsmag sikeres futtatását követően egy olyan objektumot ad eredményül, amely leírja az aktuális titkosított csatorna házirendjét, valamint az adatbázis-azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="01800-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="01800-109">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="01800-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="01800-110">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="01800-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="01800-111">Példák</span><span class="sxs-lookup"><span data-stu-id="01800-111">EXAMPLES</span></span>

### <span data-ttu-id="01800-112">Példa 1: az Azure SQL-adatbázisok titkosított csatornás házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="01800-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="01800-113">Ez a parancs a database01 nevű Azure SQL-adatbázis titkosított csatornájának házirendjét kapja meg a kiszolgálón, a server01.</span><span class="sxs-lookup"><span data-stu-id="01800-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="01800-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01800-114">PARAMETERS</span></span>

### <span data-ttu-id="01800-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01800-115">-DatabaseName</span></span>
<span data-ttu-id="01800-116">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01800-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="01800-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01800-117">-DefaultProfile</span></span>
<span data-ttu-id="01800-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="01800-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01800-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01800-119">-ResourceGroupName</span></span>
<span data-ttu-id="01800-120">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="01800-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="01800-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="01800-121">-ServerName</span></span>
<span data-ttu-id="01800-122">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01800-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="01800-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01800-123">-Confirm</span></span>
<span data-ttu-id="01800-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01800-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01800-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01800-125">-WhatIf</span></span>
<span data-ttu-id="01800-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01800-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01800-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01800-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01800-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01800-128">CommonParameters</span></span>
<span data-ttu-id="01800-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01800-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01800-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01800-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01800-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01800-131">INPUTS</span></span>

### <span data-ttu-id="01800-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="01800-132">None</span></span>
<span data-ttu-id="01800-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="01800-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01800-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01800-134">OUTPUTS</span></span>

### <span data-ttu-id="01800-135">Microsoft. Azure. Command. SQL. Security. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="01800-135">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="01800-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01800-136">NOTES</span></span>

## <span data-ttu-id="01800-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01800-137">RELATED LINKS</span></span>
