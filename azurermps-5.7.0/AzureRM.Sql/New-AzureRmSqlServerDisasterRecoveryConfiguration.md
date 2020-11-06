---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498732"
---
# <span data-ttu-id="a5670-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5670-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="a5670-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5670-102">SYNOPSIS</span></span>
<span data-ttu-id="a5670-103">Adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a5670-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5670-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5670-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5670-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5670-105">DESCRIPTION</span></span>
<span data-ttu-id="a5670-106">A **New-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag létrehoz egy SQL adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a5670-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a5670-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5670-107">EXAMPLES</span></span>

## <span data-ttu-id="a5670-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5670-108">PARAMETERS</span></span>

### <span data-ttu-id="a5670-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5670-109">-AsJob</span></span>
<span data-ttu-id="a5670-110">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a5670-110">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="a5670-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5670-111">-DefaultProfile</span></span>
<span data-ttu-id="a5670-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5670-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5670-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="a5670-113">-FailoverPolicy</span></span>
<span data-ttu-id="a5670-114">A feladatátvételi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5670-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="a5670-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5670-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a5670-116">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5670-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="a5670-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a5670-117">-PartnerServerName</span></span>
<span data-ttu-id="a5670-118">A partner kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5670-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="a5670-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5670-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5670-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5670-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5670-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a5670-121">-ServerName</span></span>
<span data-ttu-id="a5670-122">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5670-122">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5670-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="a5670-123">-VirtualEndpointName</span></span>
<span data-ttu-id="a5670-124">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5670-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="a5670-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5670-125">-Confirm</span></span>
<span data-ttu-id="a5670-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5670-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5670-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5670-127">-WhatIf</span></span>
<span data-ttu-id="a5670-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5670-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5670-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5670-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5670-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5670-130">CommonParameters</span></span>
<span data-ttu-id="a5670-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5670-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5670-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5670-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5670-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5670-133">INPUTS</span></span>

### <span data-ttu-id="a5670-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5670-134">None</span></span>
<span data-ttu-id="a5670-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a5670-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5670-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5670-136">OUTPUTS</span></span>

## <span data-ttu-id="a5670-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5670-137">NOTES</span></span>

## <span data-ttu-id="a5670-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5670-138">RELATED LINKS</span></span>

[<span data-ttu-id="a5670-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5670-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a5670-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5670-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a5670-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5670-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a5670-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a5670-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
