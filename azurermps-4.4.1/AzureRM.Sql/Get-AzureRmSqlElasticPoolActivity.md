---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: d78b2fafb6c633c8a0276193e9e42677de814ff3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672397"
---
# <span data-ttu-id="02fad-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="02fad-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="02fad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02fad-102">SYNOPSIS</span></span>
<span data-ttu-id="02fad-103">Egy rugalmas készleten kapja meg a műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="02fad-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02fad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02fad-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02fad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02fad-105">DESCRIPTION</span></span>
<span data-ttu-id="02fad-106">A **Get-AzureRmSqlElasticPoolActivity** parancsmag a műveletek állapotát az Azure SQL-adatbázisok rugalmas készletében kapja.</span><span class="sxs-lookup"><span data-stu-id="02fad-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="02fad-107">A Pool-készítési és a konfigurációs frissítések állapotát is láthatja.</span><span class="sxs-lookup"><span data-stu-id="02fad-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="02fad-108">Példák</span><span class="sxs-lookup"><span data-stu-id="02fad-108">EXAMPLES</span></span>

### <span data-ttu-id="02fad-109">Példa 1: műveletek állapotának megszerzése rugalmas készlet esetén</span><span class="sxs-lookup"><span data-stu-id="02fad-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="02fad-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="02fad-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="02fad-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02fad-111">PARAMETERS</span></span>

### <span data-ttu-id="02fad-112">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="02fad-112">-ElasticPoolName</span></span>
<span data-ttu-id="02fad-113">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02fad-113">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="02fad-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02fad-114">-ResourceGroupName</span></span>
<span data-ttu-id="02fad-115">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="02fad-115">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="02fad-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="02fad-116">-ServerName</span></span>
<span data-ttu-id="02fad-117">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02fad-117">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="02fad-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02fad-118">-Confirm</span></span>
<span data-ttu-id="02fad-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02fad-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02fad-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fad-120">-WhatIf</span></span>
<span data-ttu-id="02fad-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02fad-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02fad-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02fad-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02fad-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fad-123">-DefaultProfile</span></span>
<span data-ttu-id="02fad-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02fad-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02fad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fad-125">CommonParameters</span></span>
<span data-ttu-id="02fad-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02fad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fad-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02fad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fad-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02fad-128">INPUTS</span></span>

## <span data-ttu-id="02fad-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02fad-129">OUTPUTS</span></span>

### <span data-ttu-id="02fad-130">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="02fad-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="02fad-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02fad-131">NOTES</span></span>

## <span data-ttu-id="02fad-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02fad-132">RELATED LINKS</span></span>

[<span data-ttu-id="02fad-133">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02fad-133">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="02fad-134">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="02fad-134">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="02fad-135">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02fad-135">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="02fad-136">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02fad-136">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="02fad-137">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="02fad-137">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


