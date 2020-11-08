---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015971"
---
# <span data-ttu-id="86e7e-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="86e7e-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="86e7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="86e7e-103">Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="86e7e-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="86e7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86e7e-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e7e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="86e7e-106">A **New-AzureSqlDatabaseServer** parancsmag az Azure SQL Database Server egy példányát hozza létre az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="86e7e-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="86e7e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86e7e-107">EXAMPLES</span></span>

### <span data-ttu-id="86e7e-108">Példa 1: kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="86e7e-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="86e7e-109">Ez a parancs a 11-es verziójú Azure SQL-adatbázis kiszolgálóját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="86e7e-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="86e7e-110">2. példa: a 12-es verziójú kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="86e7e-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="86e7e-111">Ez a parancs a 12-es verziójú kiszolgálót hozza létre.</span><span class="sxs-lookup"><span data-stu-id="86e7e-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="86e7e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86e7e-112">PARAMETERS</span></span>

### <span data-ttu-id="86e7e-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="86e7e-113">-AdministratorLogin</span></span>
<span data-ttu-id="86e7e-114">Az új Azure SQL adatbázis-kiszolgáló rendszergazdai fiókjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86e7e-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="86e7e-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="86e7e-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="86e7e-116">Az Azure SQL adatbázis-kiszolgáló rendszergazdai fiókjának jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="86e7e-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="86e7e-117">Meg kell adnia egy erős jelszót.</span><span class="sxs-lookup"><span data-stu-id="86e7e-117">You must specify a strong password.</span></span>
<span data-ttu-id="86e7e-118">További információt az [erős jelszavak](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) a Microsoft fejlesztői hálózata) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86e7e-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="86e7e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="86e7e-119">-Force</span></span>
<span data-ttu-id="86e7e-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="86e7e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="86e7e-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="86e7e-121">-Location</span></span>
<span data-ttu-id="86e7e-122">Annak az adatközpontnak a helyét adja meg, ahol ez a parancsmag hozza létre a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="86e7e-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="86e7e-123">További információt az [Azure Regions](https://azure.microsoft.com/regions/) ( https://azure.microsoft.com/regions/#services) Azure-tárban) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86e7e-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="86e7e-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="86e7e-124">-Profile</span></span>
<span data-ttu-id="86e7e-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="86e7e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86e7e-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="86e7e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86e7e-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="86e7e-127">-Version</span></span>
<span data-ttu-id="86e7e-128">Az új kiszolgáló verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="86e7e-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="86e7e-129">Az érvényes értékek: 2,0 és 12,0.</span><span class="sxs-lookup"><span data-stu-id="86e7e-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e7e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86e7e-130">-Confirm</span></span>
<span data-ttu-id="86e7e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86e7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e7e-132">-WhatIf</span></span>
<span data-ttu-id="86e7e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86e7e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e7e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86e7e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e7e-135">CommonParameters</span></span>
<span data-ttu-id="86e7e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86e7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e7e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86e7e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e7e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e7e-138">INPUTS</span></span>

## <span data-ttu-id="86e7e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e7e-139">OUTPUTS</span></span>

### <span data-ttu-id="86e7e-140">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="86e7e-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="86e7e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86e7e-141">NOTES</span></span>

## <span data-ttu-id="86e7e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86e7e-142">RELATED LINKS</span></span>

[<span data-ttu-id="86e7e-143">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="86e7e-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="86e7e-144">Kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="86e7e-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="86e7e-145">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="86e7e-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="86e7e-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="86e7e-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="86e7e-147">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="86e7e-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="86e7e-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="86e7e-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


