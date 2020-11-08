---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015570"
---
# <span data-ttu-id="caaa5-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="caaa5-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="caaa5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="caaa5-102">SYNOPSIS</span></span>
<span data-ttu-id="caaa5-103">Egy Azure SQL-adatbázis-kiszolgáló kvótájának adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="caaa5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="caaa5-104">SYNTAX</span></span>

### <span data-ttu-id="caaa5-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="caaa5-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="caaa5-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="caaa5-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="caaa5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="caaa5-107">DESCRIPTION</span></span>
<span data-ttu-id="caaa5-108">A **Get-AzureSqlDatabaseServerQuota** parancsmag az Azure SQL Database Server adott példányához tartozó kvóta-információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="caaa5-109">Adja meg a kapcsolati környezetet vagy a kiszolgáló nevét.</span><span class="sxs-lookup"><span data-stu-id="caaa5-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="caaa5-110">Ha nem ad meg kvóta-nevet, ez a parancsmag a kiszolgáló összes kvóta-adatát kapja.</span><span class="sxs-lookup"><span data-stu-id="caaa5-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="caaa5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="caaa5-111">EXAMPLES</span></span>

### <span data-ttu-id="caaa5-112">1. példa: információk beszerzése adott kvótához</span><span class="sxs-lookup"><span data-stu-id="caaa5-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="caaa5-113">Ez a parancs az Premium_Databases nevű kvótát a $Context változóban tárolt kapcsolat által megadott Azure SQL adatbázis-kiszolgálóról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="caaa5-114">2. példa: információk kérése az összes kvótáról</span><span class="sxs-lookup"><span data-stu-id="caaa5-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="caaa5-115">Ez a parancs minden kvóta értékét a kapcsolat $Context által megadott kiszolgálóról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="caaa5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="caaa5-116">PARAMETERS</span></span>

### <span data-ttu-id="caaa5-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="caaa5-117">-ConnectionContext</span></span>
<span data-ttu-id="caaa5-118">A kiszolgáló kapcsolati környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caaa5-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="caaa5-119">-Profile</span></span>
<span data-ttu-id="caaa5-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="caaa5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="caaa5-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="caaa5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="caaa5-122">-QuotaName</span><span class="sxs-lookup"><span data-stu-id="caaa5-122">-QuotaName</span></span>
<span data-ttu-id="caaa5-123">Megadja annak a kvóta-értéknek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="caaa5-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caaa5-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="caaa5-124">-ServerName</span></span>
<span data-ttu-id="caaa5-125">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-125">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="caaa5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caaa5-126">CommonParameters</span></span>
<span data-ttu-id="caaa5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="caaa5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caaa5-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caaa5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caaa5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="caaa5-129">INPUTS</span></span>

## <span data-ttu-id="caaa5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caaa5-130">OUTPUTS</span></span>

### <span data-ttu-id="caaa5-131">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="caaa5-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="caaa5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="caaa5-132">NOTES</span></span>
* <span data-ttu-id="caaa5-133">Hitelesítés: Ez a parancsmag az SQL Server-hitelesítést vagy a tanúsítvány-alapú hitelesítést egyaránt használhatja.</span><span class="sxs-lookup"><span data-stu-id="caaa5-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="caaa5-134">A hitelesítés beállításának példáit a New-AzureSqlDatabaseServerContext parancsmagban találhatja meg.</span><span class="sxs-lookup"><span data-stu-id="caaa5-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="caaa5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caaa5-135">RELATED LINKS</span></span>

[<span data-ttu-id="caaa5-136">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="caaa5-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="caaa5-137">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="caaa5-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="caaa5-138">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="caaa5-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


