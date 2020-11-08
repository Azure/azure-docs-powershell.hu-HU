---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015571"
---
# <span data-ttu-id="25400-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="25400-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="25400-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25400-102">SYNOPSIS</span></span>
<span data-ttu-id="25400-103">Információt kap az Azure SQL-adatbázis kiszolgálóiról.</span><span class="sxs-lookup"><span data-stu-id="25400-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="25400-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25400-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25400-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25400-105">DESCRIPTION</span></span>
<span data-ttu-id="25400-106">A **Get-AzureSqlDatabaseServer** parancsmag információt kap az Azure SQL Database Server példányairól az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="25400-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="25400-107">Ha a kiszolgálót név szerint adja meg, ez a parancsmag egy olyan objektumot ad eredményül, amely a kiszolgálón lévő információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="25400-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="25400-108">Egyéb esetben a parancsmag az összes kiszolgálóról ad információt.</span><span class="sxs-lookup"><span data-stu-id="25400-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="25400-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25400-109">EXAMPLES</span></span>

### <span data-ttu-id="25400-110">1. példa: információk kérése az összes kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="25400-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="25400-111">Ez a parancs a jelenlegi előfizetésben az Azure SQL-adatbázis kiszolgálójának összes példányáról ad információt.</span><span class="sxs-lookup"><span data-stu-id="25400-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="25400-112">2. példa: információk kérése egy adott kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="25400-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="25400-113">Ez a parancs információt ad eredményül a lpqd0zbr8y nevű kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="25400-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="25400-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25400-114">PARAMETERS</span></span>

### <span data-ttu-id="25400-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="25400-115">-Profile</span></span>
<span data-ttu-id="25400-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="25400-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25400-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="25400-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25400-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="25400-118">-ServerName</span></span>
<span data-ttu-id="25400-119">Annak a kiszolgálónak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="25400-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="25400-120">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="25400-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="25400-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25400-121">CommonParameters</span></span>
<span data-ttu-id="25400-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25400-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25400-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25400-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25400-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25400-124">INPUTS</span></span>

### <span data-ttu-id="25400-125">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="25400-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="25400-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25400-126">OUTPUTS</span></span>

### <span data-ttu-id="25400-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="25400-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="25400-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25400-128">NOTES</span></span>

## <span data-ttu-id="25400-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25400-129">RELATED LINKS</span></span>

[<span data-ttu-id="25400-130">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="25400-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="25400-131">Kiszolgálók listája</span><span class="sxs-lookup"><span data-stu-id="25400-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="25400-132">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="25400-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="25400-133">Új – AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="25400-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="25400-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="25400-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="25400-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="25400-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


