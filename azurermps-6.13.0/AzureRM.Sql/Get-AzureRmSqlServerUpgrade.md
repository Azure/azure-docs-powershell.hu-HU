---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 7f48385c7002f353ca34f399d40310a9e0469977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492721"
---
# <span data-ttu-id="4d669-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4d669-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="4d669-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d669-102">SYNOPSIS</span></span>
<span data-ttu-id="4d669-103">Az Azure SQL-adatbázis kiszolgálói frissítésének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d669-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d669-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d669-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d669-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d669-105">DESCRIPTION</span></span>
<span data-ttu-id="4d669-106">A **Get-AzureRmSqlServerUpgrade** parancsmag az Azure SQL adatbázis-kiszolgáló frissítésének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d669-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="4d669-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4d669-107">EXAMPLES</span></span>

### <span data-ttu-id="4d669-108">Példa 1: frissítés állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4d669-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="4d669-109">Ez a parancs a Server01 nevű kiszolgálóról a ResourceGroup01 nevű erőforráscsoport frissítés állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d669-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4d669-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d669-110">PARAMETERS</span></span>

### <span data-ttu-id="4d669-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d669-111">-DefaultProfile</span></span>
<span data-ttu-id="4d669-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4d669-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d669-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d669-113">-ResourceGroupName</span></span>
<span data-ttu-id="4d669-114">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="4d669-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4d669-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4d669-115">-ServerName</span></span>
<span data-ttu-id="4d669-116">Annak a kiszolgálónak a neve, amelyhez ez a parancsmag frissíti az állapotot.</span><span class="sxs-lookup"><span data-stu-id="4d669-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="4d669-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d669-117">-Confirm</span></span>
<span data-ttu-id="4d669-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d669-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d669-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d669-119">-WhatIf</span></span>
<span data-ttu-id="4d669-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d669-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d669-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d669-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d669-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d669-122">CommonParameters</span></span>
<span data-ttu-id="4d669-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d669-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d669-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d669-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d669-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d669-125">INPUTS</span></span>

### <span data-ttu-id="4d669-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4d669-126">System.String</span></span>

## <span data-ttu-id="4d669-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d669-127">OUTPUTS</span></span>

### <span data-ttu-id="4d669-128">Microsoft. Azure. Command. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="4d669-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="4d669-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d669-129">NOTES</span></span>

## <span data-ttu-id="4d669-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d669-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d669-131">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4d669-131">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4d669-132">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4d669-132">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4d669-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4d669-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


