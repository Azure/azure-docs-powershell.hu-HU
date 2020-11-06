---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492118"
---
# <span data-ttu-id="c76c4-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="c76c4-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="c76c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c76c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c76c4-103">SQL-adatbázis kiszolgálójának frissítését leállítja.</span><span class="sxs-lookup"><span data-stu-id="c76c4-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c76c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c76c4-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c76c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c76c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c76c4-106">A **stop-AzureRmSqlServerUpgrade** parancsmag leállítja egy Azure SQL-adatbázis kiszolgálójának frissítését.</span><span class="sxs-lookup"><span data-stu-id="c76c4-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="c76c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c76c4-107">EXAMPLES</span></span>

### <span data-ttu-id="c76c4-108">Példa 1: a kiszolgáló frissítésének leállítása</span><span class="sxs-lookup"><span data-stu-id="c76c4-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="c76c4-109">Ez a parancs leállítja a ResourceGroup01 nevű Server02 hozzárendelt nevű kiszolgáló frissítésére vonatkozó kérést.</span><span class="sxs-lookup"><span data-stu-id="c76c4-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c76c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c76c4-110">PARAMETERS</span></span>

### <span data-ttu-id="c76c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76c4-111">-DefaultProfile</span></span>
<span data-ttu-id="c76c4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c76c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c76c4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c76c4-113">-Force</span></span>
<span data-ttu-id="c76c4-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c76c4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c76c4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c76c4-115">-ResourceGroupName</span></span>
<span data-ttu-id="c76c4-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="c76c4-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c76c4-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c76c4-117">-ServerName</span></span>
<span data-ttu-id="c76c4-118">Annak a kiszolgálónak a neve, amelyhez ez a parancsmag leállítja a frissítést.</span><span class="sxs-lookup"><span data-stu-id="c76c4-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="c76c4-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c76c4-119">-Confirm</span></span>
<span data-ttu-id="c76c4-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c76c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c76c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c76c4-121">-WhatIf</span></span>
<span data-ttu-id="c76c4-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c76c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c76c4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c76c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c76c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76c4-124">CommonParameters</span></span>
<span data-ttu-id="c76c4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c76c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76c4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76c4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c76c4-127">INPUTS</span></span>

### <span data-ttu-id="c76c4-128">Microsoft. Azure. Command. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="c76c4-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="c76c4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c76c4-129">OUTPUTS</span></span>

## <span data-ttu-id="c76c4-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c76c4-130">NOTES</span></span>

## <span data-ttu-id="c76c4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c76c4-131">RELATED LINKS</span></span>

[<span data-ttu-id="c76c4-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="c76c4-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="c76c4-133">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="c76c4-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="c76c4-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c76c4-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


