---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496808"
---
# <span data-ttu-id="f62dd-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f62dd-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="f62dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f62dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f62dd-103">Kiszolgáló hosszú távú adatmegőrzési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="f62dd-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f62dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f62dd-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f62dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f62dd-105">DESCRIPTION</span></span>
<span data-ttu-id="f62dd-106">A **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** parancsmag az adatbázishoz regisztrált hosszú távú adatmegőrzési házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="f62dd-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="f62dd-107">A házirend a biztonságimásolat-tárolási házirend definiálására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f62dd-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="f62dd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f62dd-108">EXAMPLES</span></span>

## <span data-ttu-id="f62dd-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f62dd-109">PARAMETERS</span></span>

### <span data-ttu-id="f62dd-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f62dd-110">-DatabaseName</span></span>
<span data-ttu-id="f62dd-111">Annak az SQL-adatbázisnak a neve, amelyhez a parancsmag házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="f62dd-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="f62dd-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62dd-112">-ResourceGroupName</span></span>
<span data-ttu-id="f62dd-113">Az adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f62dd-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="f62dd-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f62dd-114">-ResourceId</span></span>
<span data-ttu-id="f62dd-115">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f62dd-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f62dd-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f62dd-116">-ServerName</span></span>
<span data-ttu-id="f62dd-117">Itt adhatja meg az adatbázist tároló kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f62dd-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="f62dd-118">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f62dd-118">-State</span></span>
<span data-ttu-id="f62dd-119">Egy államot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f62dd-119">Specifies a state.</span></span>

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

### <span data-ttu-id="f62dd-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f62dd-120">-Confirm</span></span>
<span data-ttu-id="f62dd-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f62dd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62dd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f62dd-122">-WhatIf</span></span>
<span data-ttu-id="f62dd-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f62dd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f62dd-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f62dd-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f62dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62dd-125">-DefaultProfile</span></span>
<span data-ttu-id="f62dd-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f62dd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f62dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62dd-127">CommonParameters</span></span>
<span data-ttu-id="f62dd-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f62dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62dd-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f62dd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62dd-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f62dd-130">INPUTS</span></span>

## <span data-ttu-id="f62dd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f62dd-131">OUTPUTS</span></span>

## <span data-ttu-id="f62dd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f62dd-132">NOTES</span></span>

## <span data-ttu-id="f62dd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f62dd-133">RELATED LINKS</span></span>

[<span data-ttu-id="f62dd-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f62dd-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f62dd-135">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f62dd-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
