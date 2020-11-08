---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016563"
---
# <span data-ttu-id="1917f-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="1917f-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="1917f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1917f-102">SYNOPSIS</span></span>
<span data-ttu-id="1917f-103">Egy SQL-adatbázis méretének és méretének korlátja.</span><span class="sxs-lookup"><span data-stu-id="1917f-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="1917f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1917f-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1917f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1917f-105">DESCRIPTION</span></span>
<span data-ttu-id="1917f-106">A **Get-AzureSqlDatabaseUsages** parancsmag az Azure SQL-adatbázisok jelenlegi méret-és mérethatárt kapja.</span><span class="sxs-lookup"><span data-stu-id="1917f-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="1917f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1917f-107">EXAMPLES</span></span>

### <span data-ttu-id="1917f-108">Példa 1: SQL-adatbázis használati adatainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="1917f-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1917f-109">Ez a parancs a Database01-on Server01 nevű SQL-adatbázis méretének és méretének korlátozását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1917f-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="1917f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1917f-110">PARAMETERS</span></span>

### <span data-ttu-id="1917f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1917f-111">-DatabaseName</span></span>
<span data-ttu-id="1917f-112">Az Azure SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1917f-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1917f-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="1917f-113">-Profile</span></span>
<span data-ttu-id="1917f-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1917f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1917f-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1917f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1917f-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1917f-116">-ServerName</span></span>
<span data-ttu-id="1917f-117">Az Azure SQL-adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1917f-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1917f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1917f-118">CommonParameters</span></span>
<span data-ttu-id="1917f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1917f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1917f-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1917f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1917f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1917f-121">INPUTS</span></span>

## <span data-ttu-id="1917f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1917f-122">OUTPUTS</span></span>

## <span data-ttu-id="1917f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1917f-123">NOTES</span></span>

## <span data-ttu-id="1917f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1917f-124">RELATED LINKS</span></span>

