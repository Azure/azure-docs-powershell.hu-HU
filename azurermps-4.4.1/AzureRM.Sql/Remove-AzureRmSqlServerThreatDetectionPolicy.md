---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493814"
---
# <span data-ttu-id="f89b4-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f89b4-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="f89b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f89b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f89b4-103">Eltávolítja a fenyegetések észlelési házirendjét egy kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="f89b4-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f89b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f89b4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f89b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f89b4-105">DESCRIPTION</span></span>
<span data-ttu-id="f89b4-106">A Remove-AzureRmSqlServerThreatDetectionPolicy parancsmag eltávolítja a fenyegetés-észlelési házirendet egy Azure SQL Server-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="f89b4-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="f89b4-107">A parancsmag használatához adja meg a ResourceGroupName és a kiszolgálónév paramétert annak a kiszolgálónak a meghatározásához, amelyből a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="f89b4-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="f89b4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f89b4-108">EXAMPLES</span></span>

### <span data-ttu-id="f89b4-109">--------------------------Példa 1: fenyegetések észlelési házirendjének eltávolítása egy adatbázishoz--------------------------</span><span class="sxs-lookup"><span data-stu-id="f89b4-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="f89b4-110">Ez a parancs eltávolítja a fenyegetések észlelése házirendet egy Server01 nevű kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="f89b4-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="f89b4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f89b4-111">PARAMETERS</span></span>

### <span data-ttu-id="f89b4-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f89b4-112">-PassThru</span></span>
<span data-ttu-id="f89b4-113">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f89b4-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f89b4-114">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f89b4-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f89b4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f89b4-115">-ResourceGroupName</span></span>
<span data-ttu-id="f89b4-116">Annak a csoportnak a neve, amelyhez a kiszolgáló van társítva.</span><span class="sxs-lookup"><span data-stu-id="f89b4-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="f89b4-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f89b4-117">-ServerName</span></span>
<span data-ttu-id="f89b4-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f89b4-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="f89b4-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f89b4-119">-Confirm</span></span>
<span data-ttu-id="f89b4-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f89b4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89b4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f89b4-121">-WhatIf</span></span>
<span data-ttu-id="f89b4-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f89b4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f89b4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f89b4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89b4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89b4-124">-DefaultProfile</span></span>
<span data-ttu-id="f89b4-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f89b4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f89b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89b4-126">CommonParameters</span></span>
<span data-ttu-id="f89b4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f89b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89b4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89b4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89b4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f89b4-129">INPUTS</span></span>

###  
<span data-ttu-id="f89b4-130">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="f89b4-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="f89b4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f89b4-131">OUTPUTS</span></span>

### <span data-ttu-id="f89b4-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f89b4-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="f89b4-133">Ez a parancsmag egy ServerThreatDetectionPolicyModel objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f89b4-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="f89b4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f89b4-134">NOTES</span></span>

## <span data-ttu-id="f89b4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f89b4-135">RELATED LINKS</span></span>

[<span data-ttu-id="f89b4-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f89b4-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

