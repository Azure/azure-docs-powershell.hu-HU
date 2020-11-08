---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015568"
---
# <span data-ttu-id="404de-101">Get-AzureSqlDatabaseServiceObjective</span><span class="sxs-lookup"><span data-stu-id="404de-101">Get-AzureSqlDatabaseServiceObjective</span></span>

## <span data-ttu-id="404de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="404de-102">SYNOPSIS</span></span>
<span data-ttu-id="404de-103">Az Azure SQL adatbázis-kiszolgáló szolgáltatási céljainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="404de-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="404de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="404de-104">SYNTAX</span></span>

### <span data-ttu-id="404de-105">ByConnectionContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="404de-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="404de-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="404de-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="404de-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="404de-107">DESCRIPTION</span></span>
<span data-ttu-id="404de-108">A **Get-AzureSqlDatabaseServiceObjective** parancsmag az Azure SQL adatbázis-kiszolgáló szolgáltatási céljainak elérésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="404de-108">The **Get-AzureSqlDatabaseServiceObjective** cmdlet gets service objectives for an Azure SQL Database server.</span></span>
<span data-ttu-id="404de-109">A szolgáltatási célkitűzéseket a teljesítmény szintjeként említik.</span><span class="sxs-lookup"><span data-stu-id="404de-109">Service objectives are referred to as performance levels.</span></span>
<span data-ttu-id="404de-110">Ha nem ad meg szolgáltatási célkitűzést, ez a parancsmag visszaadja a megadott kiszolgáló érvényes szolgáltatási céljait.</span><span class="sxs-lookup"><span data-stu-id="404de-110">If you do not specify a service objective, this cmdlet returns all valid service objectives for the specified server.</span></span>

<span data-ttu-id="404de-111">Ez a parancsmag az alapszintű, a normál és a prémium szintű szolgáltatások szintjeire vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="404de-111">This cmdlet applies to Basic, Standard, and Premium service tiers.</span></span>

## <span data-ttu-id="404de-112">Példák</span><span class="sxs-lookup"><span data-stu-id="404de-112">EXAMPLES</span></span>

### <span data-ttu-id="404de-113">1. példa: a szolgáltatás összes célkitűzésének beszerzése kapcsolati környezet használatával</span><span class="sxs-lookup"><span data-stu-id="404de-113">Example 1: Get all the service objectives by using a connection context</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

<span data-ttu-id="404de-114">Ez a parancs beilleszti a kiszolgáló összes olyan szolgáltatását, amelyre a kapcsolati környezet $Context adja meg.</span><span class="sxs-lookup"><span data-stu-id="404de-114">This command gets all the service objectives for the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="404de-115">2. példa: a szolgáltatás összes célkitűzésének beszerzése kiszolgálónév használatával</span><span class="sxs-lookup"><span data-stu-id="404de-115">Example 2: Get all the service objectives by using a server name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

<span data-ttu-id="404de-116">Ez a parancs a Server01 nevű kiszolgáló összes szolgáltatását megkapja.</span><span class="sxs-lookup"><span data-stu-id="404de-116">This command gets all the service objectives for the server named Server01.</span></span>

## <span data-ttu-id="404de-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="404de-117">PARAMETERS</span></span>

### <span data-ttu-id="404de-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="404de-118">-Context</span></span>
<span data-ttu-id="404de-119">A kiszolgáló kapcsolati környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="404de-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="404de-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="404de-120">-Profile</span></span>
<span data-ttu-id="404de-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="404de-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="404de-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="404de-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="404de-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="404de-123">-ServerName</span></span>
<span data-ttu-id="404de-124">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="404de-124">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404de-125">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="404de-125">-ServiceObjective</span></span>
<span data-ttu-id="404de-126">Itt adhatja meg azt az objektumot, amely a parancsmag által beolvasott szolgáltatás célját jelképezi.</span><span class="sxs-lookup"><span data-stu-id="404de-126">Specifies an object that represents the service objective that this cmdlet gets.</span></span>
<span data-ttu-id="404de-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="404de-127">Valid values are:</span></span> 

- <span data-ttu-id="404de-128">Alap: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="404de-128">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="404de-129">Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="404de-129">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="404de-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="404de-130">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="404de-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="404de-131">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="404de-132">\* Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="404de-132">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="404de-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="404de-133">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="404de-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="404de-134">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="404de-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="404de-135">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="404de-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="404de-136">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="404de-137">\* Standard (S3) a legújabb SQL-adatbázis-frissítés V12 (előzetes verzió) része.</span><span class="sxs-lookup"><span data-stu-id="404de-137">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="404de-138">További információt az Azure [SQL Database V12 előzetes](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) verzió () újdonságai `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` Az Azure-tárban című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="404de-138">For more information, see [What's New in the Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) (`https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/`) in the Azure library.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="404de-139">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="404de-139">-ServiceObjectiveName</span></span>
<span data-ttu-id="404de-140">A beszerzéshez használandó szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="404de-140">Specifies the name of a service objective to get.</span></span>
<span data-ttu-id="404de-141">Az érvényes értékek: Basic, S0, S1, S2, S3, P1, P2 és P3.</span><span class="sxs-lookup"><span data-stu-id="404de-141">Valid values are: Basic, S0, S1, S2, S3, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404de-142">CommonParameters</span></span>
<span data-ttu-id="404de-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="404de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404de-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="404de-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404de-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="404de-145">INPUTS</span></span>

### <span data-ttu-id="404de-146">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="404de-146">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective</span></span>

## <span data-ttu-id="404de-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="404de-147">OUTPUTS</span></span>

### <span data-ttu-id="404de-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span><span class="sxs-lookup"><span data-stu-id="404de-148">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\></span></span>

## <span data-ttu-id="404de-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="404de-149">NOTES</span></span>

## <span data-ttu-id="404de-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="404de-150">RELATED LINKS</span></span>

[<span data-ttu-id="404de-151">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="404de-151">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="404de-152">A szolgáltatási szint elérési célja</span><span class="sxs-lookup"><span data-stu-id="404de-152">Get Service Level Objective</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[<span data-ttu-id="404de-153">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="404de-153">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="404de-154">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="404de-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


