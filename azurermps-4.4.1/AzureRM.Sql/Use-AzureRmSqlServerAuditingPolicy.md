---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499931"
---
# <span data-ttu-id="da4b5-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da4b5-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="da4b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="da4b5-103">Azt adja meg, hogy egy adatbázis az állomás-kiszolgáló naplózási házirendjét használja.</span><span class="sxs-lookup"><span data-stu-id="da4b5-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da4b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da4b5-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da4b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da4b5-105">DESCRIPTION</span></span>
<span data-ttu-id="da4b5-106">A **use-AzureRmSqlServerAuditingPolicy** parancsmag azt adja meg, hogy egy adatbázis az állomás-kiszolgáló naplózási házirendjét használja.</span><span class="sxs-lookup"><span data-stu-id="da4b5-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="da4b5-107">Adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="da4b5-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="da4b5-108">Ha nincs beállítva naplózási házirend az adatbázis-kiszolgálóhoz, ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="da4b5-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="da4b5-109">Ha az állomás kiszolgálói szintű naplózást használ, a fenyegetések észlelése törlődik.</span><span class="sxs-lookup"><span data-stu-id="da4b5-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="da4b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="da4b5-110">EXAMPLES</span></span>

### <span data-ttu-id="da4b5-111">1. példa: adatbázis beállítása a kiszolgáló naplózási házirendjének használatához</span><span class="sxs-lookup"><span data-stu-id="da4b5-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="da4b5-112">Ez a parancs azt adja meg, hogy a Server02 Database01 nevű adatbázis a kiszolgáló naplózási házirendjét használja.</span><span class="sxs-lookup"><span data-stu-id="da4b5-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="da4b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da4b5-113">PARAMETERS</span></span>

### <span data-ttu-id="da4b5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da4b5-114">-DatabaseName</span></span>
<span data-ttu-id="da4b5-115">Annak az adatbázisnak a neve, amely a naplózási házirendet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="da4b5-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="da4b5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da4b5-116">-PassThru</span></span>
<span data-ttu-id="da4b5-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="da4b5-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da4b5-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="da4b5-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da4b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da4b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="da4b5-120">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="da4b5-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="da4b5-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="da4b5-121">-ServerName</span></span>
<span data-ttu-id="da4b5-122">Megadja a naplózási házirendet használó adatbázist tároló kiszolgáló nevét.</span><span class="sxs-lookup"><span data-stu-id="da4b5-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="da4b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4b5-123">-DefaultProfile</span></span>
<span data-ttu-id="da4b5-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da4b5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da4b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4b5-125">CommonParameters</span></span>
<span data-ttu-id="da4b5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da4b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4b5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4b5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da4b5-128">INPUTS</span></span>

## <span data-ttu-id="da4b5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da4b5-129">OUTPUTS</span></span>

### <span data-ttu-id="da4b5-130">Microsoft. Azure. Command. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="da4b5-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="da4b5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da4b5-131">NOTES</span></span>

## <span data-ttu-id="da4b5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da4b5-132">RELATED LINKS</span></span>

[<span data-ttu-id="da4b5-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da4b5-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="da4b5-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da4b5-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="da4b5-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da4b5-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="da4b5-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da4b5-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="da4b5-137">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="da4b5-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


