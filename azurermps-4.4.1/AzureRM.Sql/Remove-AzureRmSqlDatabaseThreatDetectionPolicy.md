---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 723e765435aae739e6d58320276f7df8ac06ba66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505587"
---
# <span data-ttu-id="d18f4-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d18f4-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="d18f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d18f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d18f4-103">Eltávolítja a fenyegetések észlelési házirendjét egy adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="d18f4-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d18f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d18f4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d18f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d18f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d18f4-106">A **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** parancsmag eltávolítja a fenyegetés-észlelési házirendet egy AzureAzure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="d18f4-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="d18f4-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak az adatbázisnak a meghatározásához, amelyből a parancsmag eltávolítja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="d18f4-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="d18f4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d18f4-108">EXAMPLES</span></span>

### <span data-ttu-id="d18f4-109">1. példa: fenyegetések észlelési házirendjének eltávolítása egy adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="d18f4-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d18f4-110">Ez a parancs eltávolítja a fenyegetés észlelési házirendjét egy Database01 nevű adatbázisból a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="d18f4-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="d18f4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d18f4-111">PARAMETERS</span></span>

### <span data-ttu-id="d18f4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d18f4-112">-DatabaseName</span></span>
<span data-ttu-id="d18f4-113">Annak az adatbázisnak a nevét adja meg, amelyben a fenyegetések észlelése házirendet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="d18f4-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="d18f4-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d18f4-114">-PassThru</span></span>
<span data-ttu-id="d18f4-115">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d18f4-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d18f4-116">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d18f4-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d18f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d18f4-118">Annak a csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="d18f4-118">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="d18f4-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d18f4-119">-ServerName</span></span>
<span data-ttu-id="d18f4-120">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis fut.</span><span class="sxs-lookup"><span data-stu-id="d18f4-120">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="d18f4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d18f4-121">-Confirm</span></span>
<span data-ttu-id="d18f4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d18f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18f4-123">-WhatIf</span></span>
<span data-ttu-id="d18f4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d18f4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d18f4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d18f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18f4-126">-DefaultProfile</span></span>
<span data-ttu-id="d18f4-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d18f4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d18f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18f4-128">CommonParameters</span></span>
<span data-ttu-id="d18f4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d18f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18f4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18f4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d18f4-131">INPUTS</span></span>

###  
<span data-ttu-id="d18f4-132">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="d18f4-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="d18f4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d18f4-133">OUTPUTS</span></span>

### <span data-ttu-id="d18f4-134">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d18f4-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="d18f4-135">Ez a parancsmag egy **DatabaseThreatDetectionPolicyModel** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d18f4-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="d18f4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d18f4-136">NOTES</span></span>

## <span data-ttu-id="d18f4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d18f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="d18f4-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d18f4-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


