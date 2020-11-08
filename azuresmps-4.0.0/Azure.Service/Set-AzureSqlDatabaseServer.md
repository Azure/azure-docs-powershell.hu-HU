---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015864"
---
# <span data-ttu-id="4f231-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4f231-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="4f231-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f231-102">SYNOPSIS</span></span>
<span data-ttu-id="4f231-103">Módosítja egy Azure SQL-adatbázis kiszolgálójának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4f231-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="4f231-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f231-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f231-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f231-105">DESCRIPTION</span></span>
<span data-ttu-id="4f231-106">A **set-AzureSqlDatabaseServer** parancsmag az Azure SQL Database Server adott példányának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="4f231-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="4f231-107">Az aktuális kiadásban csak a kiszolgáló rendszergazdai fiók jelszavát tudja frissíteni.</span><span class="sxs-lookup"><span data-stu-id="4f231-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="4f231-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4f231-108">EXAMPLES</span></span>

### <span data-ttu-id="4f231-109">Példa 1: a kiszolgáló jelszavának módosítása</span><span class="sxs-lookup"><span data-stu-id="4f231-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="4f231-110">Ez a parancs módosítja a lpqd0zbr8y nevű Azure SQL Database Server rendszergazdai fiókjának jelszavát.</span><span class="sxs-lookup"><span data-stu-id="4f231-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="4f231-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f231-111">PARAMETERS</span></span>

### <span data-ttu-id="4f231-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="4f231-112">-AdminPassword</span></span>
<span data-ttu-id="4f231-113">Az Azure SQL adatbázis-kiszolgáló rendszergazdai fiókjának jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f231-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="4f231-114">Meg kell adnia egy erős jelszót.</span><span class="sxs-lookup"><span data-stu-id="4f231-114">You must specify a strong password.</span></span>
<span data-ttu-id="4f231-115">További információt az [erős jelszavak](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) a Microsoft fejlesztői hálózata) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f231-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="4f231-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4f231-116">-Force</span></span>
<span data-ttu-id="4f231-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4f231-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f231-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f231-118">-Profile</span></span>
<span data-ttu-id="4f231-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4f231-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f231-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4f231-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f231-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4f231-121">-ServerName</span></span>
<span data-ttu-id="4f231-122">Itt adhatja meg annak a kiszolgálónak a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="4f231-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="4f231-123">Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.</span><span class="sxs-lookup"><span data-stu-id="4f231-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="4f231-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f231-124">-Confirm</span></span>
<span data-ttu-id="4f231-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f231-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f231-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f231-126">-WhatIf</span></span>
<span data-ttu-id="4f231-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f231-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f231-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f231-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f231-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f231-129">CommonParameters</span></span>
<span data-ttu-id="4f231-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f231-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f231-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f231-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f231-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f231-132">INPUTS</span></span>

### <span data-ttu-id="4f231-133">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="4f231-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="4f231-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f231-134">OUTPUTS</span></span>

## <span data-ttu-id="4f231-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f231-135">NOTES</span></span>

## <span data-ttu-id="4f231-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f231-136">RELATED LINKS</span></span>

[<span data-ttu-id="4f231-137">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="4f231-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4f231-138">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="4f231-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4f231-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4f231-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="4f231-140">Új – AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4f231-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="4f231-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="4f231-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


