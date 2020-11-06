---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493342"
---
# <span data-ttu-id="11950-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="11950-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="11950-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11950-102">SYNOPSIS</span></span>
<span data-ttu-id="11950-103">Az Azure SQL-adatbázis kiszolgálói frissítésének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11950-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11950-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11950-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11950-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11950-105">DESCRIPTION</span></span>
<span data-ttu-id="11950-106">A **Get-AzureRmSqlServerUpgrade** parancsmag az Azure SQL adatbázis-kiszolgáló frissítésének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11950-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="11950-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11950-107">EXAMPLES</span></span>

### <span data-ttu-id="11950-108">Példa 1: frissítés állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="11950-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="11950-109">Ez a parancs a Server01 nevű kiszolgálóról a ResourceGroup01 nevű erőforráscsoport frissítés állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11950-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="11950-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11950-110">PARAMETERS</span></span>

### <span data-ttu-id="11950-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11950-111">-ResourceGroupName</span></span>
<span data-ttu-id="11950-112">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="11950-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="11950-113">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="11950-113">-ServerName</span></span>
<span data-ttu-id="11950-114">Annak a kiszolgálónak a neve, amelyhez ez a parancsmag frissíti az állapotot.</span><span class="sxs-lookup"><span data-stu-id="11950-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="11950-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11950-115">-Confirm</span></span>
<span data-ttu-id="11950-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11950-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11950-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11950-117">-WhatIf</span></span>
<span data-ttu-id="11950-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11950-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11950-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11950-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11950-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11950-120">-DefaultProfile</span></span>
<span data-ttu-id="11950-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11950-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11950-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11950-122">CommonParameters</span></span>
<span data-ttu-id="11950-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11950-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11950-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11950-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11950-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11950-125">INPUTS</span></span>

## <span data-ttu-id="11950-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11950-126">OUTPUTS</span></span>

### <span data-ttu-id="11950-127">Microsoft. Azure. Command. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="11950-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="11950-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11950-128">NOTES</span></span>

## <span data-ttu-id="11950-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11950-129">RELATED LINKS</span></span>

[<span data-ttu-id="11950-130">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="11950-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="11950-131">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="11950-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="11950-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="11950-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


