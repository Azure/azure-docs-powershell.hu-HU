---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680749"
---
# <span data-ttu-id="aa4ba-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa4ba-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="aa4ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4ba-103">Módosítja az adatbázis-kiszolgáló helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa4ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa4ba-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa4ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa4ba-105">DESCRIPTION</span></span>
<span data-ttu-id="aa4ba-106">A **set-AzureRmSqlServerDisasterRecoveryConfiguration** parancsmag módosította az SQL-adatbázis kiszolgálójának helyreállítási konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="aa4ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa4ba-107">EXAMPLES</span></span>

## <span data-ttu-id="aa4ba-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa4ba-108">PARAMETERS</span></span>

### <span data-ttu-id="aa4ba-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="aa4ba-109">-AllowDataLoss</span></span>
<span data-ttu-id="aa4ba-110">Jelzi, hogy a feladatátvételi művelet lehetővé teszi az adatvesztést.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-110">Indicates that the failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ba-111">-Feladatátvétel</span><span class="sxs-lookup"><span data-stu-id="aa4ba-111">-Failover</span></span>
<span data-ttu-id="aa4ba-112">Jelzi, hogy ez a művelet feladatátvétel.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-112">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ba-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4ba-113">-ResourceGroupName</span></span>
<span data-ttu-id="aa4ba-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aa4ba-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="aa4ba-115">-ServerName</span></span>
<span data-ttu-id="aa4ba-116">Egy SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="aa4ba-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="aa4ba-117">-VirtualEndpointName</span></span>
<span data-ttu-id="aa4ba-118">A virtuális végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="aa4ba-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa4ba-119">-Confirm</span></span>
<span data-ttu-id="aa4ba-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa4ba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa4ba-121">-WhatIf</span></span>
<span data-ttu-id="aa4ba-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa4ba-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa4ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4ba-124">-DefaultProfile</span></span>
<span data-ttu-id="aa4ba-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa4ba-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa4ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4ba-126">CommonParameters</span></span>
<span data-ttu-id="aa4ba-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa4ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4ba-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4ba-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa4ba-129">INPUTS</span></span>

## <span data-ttu-id="aa4ba-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa4ba-130">OUTPUTS</span></span>

## <span data-ttu-id="aa4ba-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa4ba-131">NOTES</span></span>

## <span data-ttu-id="aa4ba-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa4ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa4ba-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa4ba-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="aa4ba-134">Új – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa4ba-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="aa4ba-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa4ba-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="aa4ba-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa4ba-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
