---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495611"
---
# <span data-ttu-id="7d311-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="7d311-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="7d311-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d311-102">SYNOPSIS</span></span>
<span data-ttu-id="7d311-103">Az adatbázis-kiszolgálói rendszer-helyreállítási konfiguráció tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="7d311-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d311-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d311-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d311-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d311-105">DESCRIPTION</span></span>
<span data-ttu-id="7d311-106">A **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** PARANCSMAG az SQL-adatbázis kiszolgálói rendszer-helyreállítási konfigurációjának tevékenységeit kapja.</span><span class="sxs-lookup"><span data-stu-id="7d311-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="7d311-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7d311-107">EXAMPLES</span></span>

## <span data-ttu-id="7d311-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d311-108">PARAMETERS</span></span>

### <span data-ttu-id="7d311-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d311-109">-DefaultProfile</span></span>
<span data-ttu-id="7d311-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d311-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d311-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7d311-111">-OperationId</span></span>
<span data-ttu-id="7d311-112">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d311-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="7d311-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d311-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d311-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d311-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7d311-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7d311-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="7d311-116">A kiszolgálói rendszer-helyreállítási konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d311-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="7d311-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7d311-117">-ServerName</span></span>
<span data-ttu-id="7d311-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d311-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7d311-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d311-119">-Confirm</span></span>
<span data-ttu-id="7d311-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d311-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d311-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d311-121">-WhatIf</span></span>
<span data-ttu-id="7d311-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d311-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d311-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d311-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d311-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d311-124">CommonParameters</span></span>
<span data-ttu-id="7d311-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d311-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d311-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d311-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d311-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d311-127">INPUTS</span></span>

### <span data-ttu-id="7d311-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7d311-128">System.String</span></span>

### <span data-ttu-id="7d311-129">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7d311-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7d311-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d311-130">OUTPUTS</span></span>

### <span data-ttu-id="7d311-131">Microsoft. Azure. Command. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="7d311-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="7d311-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d311-132">NOTES</span></span>

## <span data-ttu-id="7d311-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d311-133">RELATED LINKS</span></span>

[<span data-ttu-id="7d311-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7d311-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
