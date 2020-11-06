---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a0dc151c86caf41131649f7e4e37ee60c6f19b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498164"
---
# <span data-ttu-id="2de7c-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="2de7c-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="2de7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2de7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2de7c-103">Azt adja meg, hogy egy adatbázis az állomás-kiszolgáló naplózási házirendjét használja.</span><span class="sxs-lookup"><span data-stu-id="2de7c-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2de7c-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2de7c-105">DESCRIPTION</span></span>
<span data-ttu-id="2de7c-106">A **use-AzureRmSqlServerAuditingPolicy** parancsmag azt adja meg, hogy egy adatbázis az állomás-kiszolgáló naplózási házirendjét használja.</span><span class="sxs-lookup"><span data-stu-id="2de7c-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="2de7c-107">Adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert az adatbázis meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="2de7c-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="2de7c-108">Ha nincs beállítva naplózási házirend az adatbázis-kiszolgálóhoz, ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="2de7c-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>
<span data-ttu-id="2de7c-109">Ha az állomás kiszolgálói szintű naplózást használ, a fenyegetések észlelése törlődik.</span><span class="sxs-lookup"><span data-stu-id="2de7c-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="2de7c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2de7c-110">EXAMPLES</span></span>

### <span data-ttu-id="2de7c-111">1. példa: adatbázis beállítása a kiszolgáló naplózási házirendjének használatához</span><span class="sxs-lookup"><span data-stu-id="2de7c-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="2de7c-112">Ez a parancs azt adja meg, hogy a Server02 Database01 nevű adatbázis a kiszolgáló naplózási házirendjét használja.</span><span class="sxs-lookup"><span data-stu-id="2de7c-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="2de7c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2de7c-113">PARAMETERS</span></span>

### <span data-ttu-id="2de7c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2de7c-114">-DatabaseName</span></span>
<span data-ttu-id="2de7c-115">Annak az adatbázisnak a neve, amely a naplózási házirendet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="2de7c-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="2de7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de7c-116">-DefaultProfile</span></span>
<span data-ttu-id="2de7c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2de7c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2de7c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2de7c-118">-PassThru</span></span>
<span data-ttu-id="2de7c-119">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2de7c-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2de7c-120">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2de7c-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2de7c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de7c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2de7c-122">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="2de7c-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2de7c-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2de7c-123">-ServerName</span></span>
<span data-ttu-id="2de7c-124">Megadja a naplózási házirendet használó adatbázist tároló kiszolgáló nevét.</span><span class="sxs-lookup"><span data-stu-id="2de7c-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="2de7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de7c-125">CommonParameters</span></span>
<span data-ttu-id="2de7c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2de7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de7c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de7c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de7c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2de7c-128">INPUTS</span></span>

### <span data-ttu-id="2de7c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2de7c-129">System.String</span></span>

## <span data-ttu-id="2de7c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2de7c-130">OUTPUTS</span></span>

### <span data-ttu-id="2de7c-131">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2de7c-131">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="2de7c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2de7c-132">NOTES</span></span>

## <span data-ttu-id="2de7c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2de7c-133">RELATED LINKS</span></span>

[<span data-ttu-id="2de7c-134">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="2de7c-134">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="2de7c-135">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="2de7c-135">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="2de7c-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="2de7c-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="2de7c-137">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="2de7c-137">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="2de7c-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2de7c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


