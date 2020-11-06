---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 3c67c432f8f49927af4cbf357a4338f528c826b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502339"
---
# <span data-ttu-id="e80d1-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="e80d1-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="e80d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e80d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e80d1-103">Az adatbázis-kiszolgálói rendszer-helyreállítási konfiguráció tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="e80d1-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e80d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e80d1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e80d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e80d1-105">DESCRIPTION</span></span>
<span data-ttu-id="e80d1-106">A **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** PARANCSMAG az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációjának tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="e80d1-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e80d1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e80d1-107">EXAMPLES</span></span>

## <span data-ttu-id="e80d1-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e80d1-108">PARAMETERS</span></span>

### <span data-ttu-id="e80d1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80d1-109">-DefaultProfile</span></span>
<span data-ttu-id="e80d1-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e80d1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e80d1-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e80d1-111">-OperationId</span></span>
<span data-ttu-id="e80d1-112">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e80d1-112">Specifies the operation ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80d1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e80d1-113">-ResourceGroupName</span></span>
<span data-ttu-id="e80d1-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e80d1-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e80d1-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e80d1-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="e80d1-116">A kiszolgálói rendszer-helyreállítási konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e80d1-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="e80d1-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e80d1-117">-ServerName</span></span>
<span data-ttu-id="e80d1-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e80d1-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e80d1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e80d1-119">-Confirm</span></span>
<span data-ttu-id="e80d1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e80d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e80d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e80d1-121">-WhatIf</span></span>
<span data-ttu-id="e80d1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e80d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e80d1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e80d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e80d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80d1-124">CommonParameters</span></span>
<span data-ttu-id="e80d1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e80d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80d1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e80d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80d1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e80d1-127">INPUTS</span></span>

### <span data-ttu-id="e80d1-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e80d1-128">None</span></span>
<span data-ttu-id="e80d1-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e80d1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e80d1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e80d1-130">OUTPUTS</span></span>

## <span data-ttu-id="e80d1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e80d1-131">NOTES</span></span>

## <span data-ttu-id="e80d1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e80d1-132">RELATED LINKS</span></span>

[<span data-ttu-id="e80d1-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e80d1-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
