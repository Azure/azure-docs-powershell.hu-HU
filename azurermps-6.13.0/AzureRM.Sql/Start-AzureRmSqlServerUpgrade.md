---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494865"
---
# <span data-ttu-id="b0aba-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="b0aba-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="b0aba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0aba-102">SYNOPSIS</span></span>
<span data-ttu-id="b0aba-103">SQL-adatbázis kiszolgálójának frissítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="b0aba-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0aba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0aba-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0aba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0aba-105">DESCRIPTION</span></span>
<span data-ttu-id="b0aba-106">A **Start-AzureRmSqlServerUpgrade** parancsmag az Azure SQL Database Server 11-es verziójáról a 12-es verzióra való frissítést indítja el.</span><span class="sxs-lookup"><span data-stu-id="b0aba-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="b0aba-107">A frissítés előrehaladását az Get-AzureRmSqlServerUpgrade parancsmag segítségével figyelheti.</span><span class="sxs-lookup"><span data-stu-id="b0aba-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="b0aba-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b0aba-108">EXAMPLES</span></span>

### <span data-ttu-id="b0aba-109">1. példa: kiszolgáló frissítése</span><span class="sxs-lookup"><span data-stu-id="b0aba-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="b0aba-110">Ez a parancs frissíti a server01 nevű kiszolgálót, amely az erőforráscsoport TesourceGroup01 van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="b0aba-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="b0aba-111">2. példa: a kiszolgáló frissítése az ütemezési idő és az adatbázis-javaslat használatával</span><span class="sxs-lookup"><span data-stu-id="b0aba-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="b0aba-112">Az első parancs öt perccel a jövőben hoz létre egy időpontot a Get-Date parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b0aba-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="b0aba-113">A parancs a dátumot az $ScheduleTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b0aba-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="b0aba-114">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b0aba-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b0aba-115">A második parancs létrehoz egy **RecommendedDatabaseProperties** objektumot, majd az adott objektumot az $DatabaseMap változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b0aba-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>
<span data-ttu-id="b0aba-116">A következő három parancs a $DatabaseMapban tárolt objektum tulajdonságainak értékét rendeli hozzá az értékekhez.</span><span class="sxs-lookup"><span data-stu-id="b0aba-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>
<span data-ttu-id="b0aba-117">A végleges parancs frissíti a Server01 nevű meglévő kiszolgálót a 12,0-es verzióra.</span><span class="sxs-lookup"><span data-stu-id="b0aba-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="b0aba-118">A frissítés legkorábbi időpontja öt perc a parancs futtatása után, a $ScheduleTime változóban megadott módon.</span><span class="sxs-lookup"><span data-stu-id="b0aba-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="b0aba-119">A frissítés után az adatbázis-contosodb a normál kiadást fogja futtatni, és a szolgáltatási szint objektív S0 kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b0aba-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="b0aba-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0aba-120">PARAMETERS</span></span>

### <span data-ttu-id="b0aba-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="b0aba-121">-DatabaseCollection</span></span>
<span data-ttu-id="b0aba-122">Itt adhatja meg a kiszolgáló frissítéséhez a parancsmag által használt **RecommendedDatabaseProperties** -objektumok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="b0aba-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0aba-123">-DefaultProfile</span></span>
<span data-ttu-id="b0aba-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0aba-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0aba-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="b0aba-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="b0aba-126">A kiszolgálói frissítéshez használandó **UpgradeRecommendedElasticPoolProperties** -objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0aba-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0aba-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0aba-128">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="b0aba-128">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b0aba-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="b0aba-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="b0aba-130">A kiszolgáló frissítéséhez a legkorábbi időpontot **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0aba-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="b0aba-131">Adjon meg egy értéket a ISO8601 formátumban (az egyezményes világidő (UTC)).</span><span class="sxs-lookup"><span data-stu-id="b0aba-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="b0aba-132">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b0aba-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aba-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b0aba-133">-ServerName</span></span>
<span data-ttu-id="b0aba-134">Itt adhatja meg annak a kiszolgálónak a nevét, amely a parancsmag frissítéseit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b0aba-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0aba-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="b0aba-135">-ServerVersion</span></span>
<span data-ttu-id="b0aba-136">Azt a verziót adja meg, amelyre a parancsmag frissíti a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="b0aba-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="b0aba-137">Az egyetlen érvényes érték az 12,0.</span><span class="sxs-lookup"><span data-stu-id="b0aba-137">The only valid value is 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0aba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0aba-138">CommonParameters</span></span>
<span data-ttu-id="b0aba-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0aba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0aba-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0aba-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0aba-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0aba-141">INPUTS</span></span>

### <span data-ttu-id="b0aba-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0aba-142">System.String</span></span>

## <span data-ttu-id="b0aba-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0aba-143">OUTPUTS</span></span>

### <span data-ttu-id="b0aba-144">Microsoft. Azure. Command. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeStartModel</span><span class="sxs-lookup"><span data-stu-id="b0aba-144">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeStartModel</span></span>

## <span data-ttu-id="b0aba-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0aba-145">NOTES</span></span>

## <span data-ttu-id="b0aba-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0aba-146">RELATED LINKS</span></span>

[<span data-ttu-id="b0aba-147">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="b0aba-147">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="b0aba-148">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="b0aba-148">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="b0aba-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b0aba-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


