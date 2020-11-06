---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493323"
---
# <span data-ttu-id="1d5f3-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d5f3-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="1d5f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5f3-103">Adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d5f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d5f3-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d5f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d5f3-105">DESCRIPTION</span></span>
<span data-ttu-id="1d5f3-106">A **New-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag létrehoz egy SQL adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="1d5f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1d5f3-107">EXAMPLES</span></span>

## <span data-ttu-id="1d5f3-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d5f3-108">PARAMETERS</span></span>

### <span data-ttu-id="1d5f3-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1d5f3-109">-FailoverPolicy</span></span>
<span data-ttu-id="1d5f3-110">A feladatátvételi házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-110">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d5f3-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5f3-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1d5f3-112">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="1d5f3-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1d5f3-113">-PartnerServerName</span></span>
<span data-ttu-id="1d5f3-114">A partner kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="1d5f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d5f3-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1d5f3-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1d5f3-117">-ServerName</span></span>
<span data-ttu-id="1d5f3-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1d5f3-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="1d5f3-119">-VirtualEndpointName</span></span>
<span data-ttu-id="1d5f3-120">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="1d5f3-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d5f3-121">-Confirm</span></span>
<span data-ttu-id="1d5f3-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d5f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d5f3-123">-WhatIf</span></span>
<span data-ttu-id="1d5f3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d5f3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d5f3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5f3-126">-DefaultProfile</span></span>
<span data-ttu-id="1d5f3-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d5f3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d5f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5f3-128">CommonParameters</span></span>
<span data-ttu-id="1d5f3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d5f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d5f3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d5f3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5f3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d5f3-131">INPUTS</span></span>

## <span data-ttu-id="1d5f3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d5f3-132">OUTPUTS</span></span>

## <span data-ttu-id="1d5f3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d5f3-133">NOTES</span></span>

## <span data-ttu-id="1d5f3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d5f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d5f3-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d5f3-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="1d5f3-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d5f3-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="1d5f3-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d5f3-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="1d5f3-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1d5f3-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
