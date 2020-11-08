---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016559"
---
# <span data-ttu-id="c6267-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="c6267-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="c6267-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6267-102">SYNOPSIS</span></span>
<span data-ttu-id="c6267-103">Helyreállítható adatbázisokat kap egy megadott kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="c6267-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="c6267-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6267-104">SYNTAX</span></span>

### <span data-ttu-id="c6267-105">AllDatabasesOnGivenServer (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6267-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c6267-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="c6267-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6267-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c6267-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6267-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6267-108">DESCRIPTION</span></span>
<span data-ttu-id="c6267-109">A **Get-AzureSqlRecoverableDatabase** parancsmag visszanyerhető adatbázisokat kap egy megadott kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="c6267-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="c6267-110">Ez a parancsmag meghatározott helyreállítható adatbázis vagy a kiszolgálón található összes helyreállítható adatbázis bevezetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="c6267-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="c6267-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c6267-111">EXAMPLES</span></span>

### <span data-ttu-id="c6267-112">Példa 1: a helyreállítható adatbázisok beszerzése</span><span class="sxs-lookup"><span data-stu-id="c6267-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="c6267-113">Ez a parancs a Server01 nevű kiszolgálón a helyreállítható adatbázisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6267-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="c6267-114">2. példa: meghatározott helyreállítható adatbázis beszerzése</span><span class="sxs-lookup"><span data-stu-id="c6267-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="c6267-115">A parancs beolvassa a Database17 nevű adatbázist a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="c6267-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="c6267-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6267-116">PARAMETERS</span></span>

### <span data-ttu-id="c6267-117">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="c6267-117">-Database</span></span>
<span data-ttu-id="c6267-118">Itt adhatja meg azt az objektumot, amely a parancsmag által elérhető helyreállítható adatbázisnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="c6267-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6267-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6267-119">-DatabaseName</span></span>
<span data-ttu-id="c6267-120">Annak a helyreállítható adatbázisnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c6267-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6267-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6267-121">-Profile</span></span>
<span data-ttu-id="c6267-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c6267-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6267-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c6267-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6267-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c6267-124">-ServerName</span></span>
<span data-ttu-id="c6267-125">Annak a kiszolgálónak a neve, amelyből a parancsmag helyreállítható adatbázisokat kap.</span><span class="sxs-lookup"><span data-stu-id="c6267-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6267-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6267-126">CommonParameters</span></span>
<span data-ttu-id="c6267-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6267-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6267-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6267-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6267-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6267-129">INPUTS</span></span>

### <span data-ttu-id="c6267-130">Microsoft. WindowsAzure. Management. SQL. models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="c6267-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="c6267-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6267-131">OUTPUTS</span></span>

### <span data-ttu-id="c6267-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="c6267-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="c6267-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6267-133">NOTES</span></span>
* <span data-ttu-id="c6267-134">A parancsmag futtatásához tanúsítványon alapuló hitelesítést kell használnia.</span><span class="sxs-lookup"><span data-stu-id="c6267-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="c6267-135">Futtassa az alábbi parancsokat azon a számítógépen, amelyen a parancsmag futtatható:</span><span class="sxs-lookup"><span data-stu-id="c6267-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="c6267-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6267-136">RELATED LINKS</span></span>

[<span data-ttu-id="c6267-137">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="c6267-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c6267-138">Helyreállítható adatbázis beszerzése</span><span class="sxs-lookup"><span data-stu-id="c6267-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="c6267-139">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="c6267-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c6267-140">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="c6267-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


