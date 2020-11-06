---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 792d72c509df4c6b84f4ea86e597ddd8040a30d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502891"
---
# <span data-ttu-id="690c0-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="690c0-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="690c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="690c0-102">SYNOPSIS</span></span>
<span data-ttu-id="690c0-103">Adatbázis-kiszolgáló rendszer-helyreállítási konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="690c0-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="690c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="690c0-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="690c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="690c0-105">DESCRIPTION</span></span>
<span data-ttu-id="690c0-106">A **Get-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag SQL adatbázis-kiszolgálói rendszer-helyreállítási konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="690c0-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="690c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="690c0-107">EXAMPLES</span></span>

## <span data-ttu-id="690c0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="690c0-108">PARAMETERS</span></span>

### <span data-ttu-id="690c0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690c0-109">-DefaultProfile</span></span>
<span data-ttu-id="690c0-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="690c0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="690c0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690c0-111">-ResourceGroupName</span></span>
<span data-ttu-id="690c0-112">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="690c0-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="690c0-113">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="690c0-113">-ServerName</span></span>
<span data-ttu-id="690c0-114">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="690c0-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="690c0-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="690c0-115">-VirtualEndpointName</span></span>
<span data-ttu-id="690c0-116">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="690c0-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="690c0-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="690c0-117">-Confirm</span></span>
<span data-ttu-id="690c0-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="690c0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="690c0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690c0-119">-WhatIf</span></span>
<span data-ttu-id="690c0-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="690c0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="690c0-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="690c0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="690c0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690c0-122">CommonParameters</span></span>
<span data-ttu-id="690c0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="690c0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690c0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690c0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690c0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="690c0-125">INPUTS</span></span>

### <span data-ttu-id="690c0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="690c0-126">System.String</span></span>

## <span data-ttu-id="690c0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="690c0-127">OUTPUTS</span></span>

### <span data-ttu-id="690c0-128">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="690c0-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="690c0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="690c0-129">NOTES</span></span>

## <span data-ttu-id="690c0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="690c0-130">RELATED LINKS</span></span>

[<span data-ttu-id="690c0-131">Új – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="690c0-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="690c0-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="690c0-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="690c0-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="690c0-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="690c0-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="690c0-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
