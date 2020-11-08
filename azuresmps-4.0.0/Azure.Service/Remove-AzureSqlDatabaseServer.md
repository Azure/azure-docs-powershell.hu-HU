---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016107"
---
# <span data-ttu-id="f9952-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f9952-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="f9952-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9952-102">SYNOPSIS</span></span>
<span data-ttu-id="f9952-103">Azure SQL-adatbázis kiszolgálójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f9952-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="f9952-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9952-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9952-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9952-105">DESCRIPTION</span></span>
<span data-ttu-id="f9952-106">A **Remove-AzureSqlDatabaseServer** parancsmag eltávolítja az Azure SQL Database Server adott példányát az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="f9952-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="f9952-107">Ez a parancsmag minden adatbázis törlését törli a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f9952-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="f9952-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f9952-108">EXAMPLES</span></span>

### <span data-ttu-id="f9952-109">1. példa: adatbázis-kiszolgáló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f9952-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="f9952-110">Ez a parancs eltávolítja a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f9952-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="f9952-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9952-111">PARAMETERS</span></span>

### <span data-ttu-id="f9952-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f9952-112">-Force</span></span>
<span data-ttu-id="f9952-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f9952-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9952-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="f9952-114">-Profile</span></span>
<span data-ttu-id="f9952-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f9952-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9952-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f9952-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9952-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f9952-117">-ServerName</span></span>
<span data-ttu-id="f9952-118">Annak a kiszolgálónak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="f9952-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="f9952-119">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="f9952-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="f9952-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9952-120">-Confirm</span></span>
<span data-ttu-id="f9952-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9952-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9952-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9952-122">-WhatIf</span></span>
<span data-ttu-id="f9952-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9952-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9952-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9952-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9952-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9952-125">CommonParameters</span></span>
<span data-ttu-id="f9952-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9952-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9952-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9952-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9952-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9952-128">INPUTS</span></span>

### <span data-ttu-id="f9952-129">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f9952-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="f9952-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9952-130">OUTPUTS</span></span>

## <span data-ttu-id="f9952-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9952-131">NOTES</span></span>

## <span data-ttu-id="f9952-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9952-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9952-133">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="f9952-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f9952-134">Kiszolgáló törlése</span><span class="sxs-lookup"><span data-stu-id="f9952-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="f9952-135">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="f9952-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f9952-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f9952-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f9952-137">Új – AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f9952-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f9952-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f9952-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


