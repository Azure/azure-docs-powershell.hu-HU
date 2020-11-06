---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 0cabae7f7b803001a03b64eec027925733d05545
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501588"
---
# <span data-ttu-id="6b189-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="6b189-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="6b189-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b189-102">SYNOPSIS</span></span>
<span data-ttu-id="6b189-103">Az adatbázis-kiszolgálói rendszer-helyreállítási konfiguráció tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="6b189-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b189-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b189-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b189-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b189-105">DESCRIPTION</span></span>
<span data-ttu-id="6b189-106">A **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** PARANCSMAG az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációjának tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="6b189-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="6b189-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6b189-107">EXAMPLES</span></span>

## <span data-ttu-id="6b189-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b189-108">PARAMETERS</span></span>

### <span data-ttu-id="6b189-109">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6b189-109">-OperationId</span></span>
<span data-ttu-id="6b189-110">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b189-110">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b189-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b189-111">-ResourceGroupName</span></span>
<span data-ttu-id="6b189-112">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b189-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6b189-113">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6b189-113">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="6b189-114">A kiszolgálói rendszer-helyreállítási konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b189-114">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b189-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6b189-115">-ServerName</span></span>
<span data-ttu-id="6b189-116">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b189-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6b189-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b189-117">-Confirm</span></span>
<span data-ttu-id="6b189-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b189-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b189-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b189-119">-WhatIf</span></span>
<span data-ttu-id="6b189-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b189-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b189-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b189-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b189-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b189-122">-DefaultProfile</span></span>
<span data-ttu-id="6b189-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b189-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b189-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b189-124">CommonParameters</span></span>
<span data-ttu-id="6b189-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b189-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b189-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b189-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b189-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b189-127">INPUTS</span></span>

## <span data-ttu-id="6b189-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b189-128">OUTPUTS</span></span>

## <span data-ttu-id="6b189-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b189-129">NOTES</span></span>

## <span data-ttu-id="6b189-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b189-130">RELATED LINKS</span></span>

[<span data-ttu-id="6b189-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6b189-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
