---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498771"
---
# <span data-ttu-id="ba269-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba269-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="ba269-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba269-102">SYNOPSIS</span></span>
<span data-ttu-id="ba269-103">Az adatbázis veszélyforrás-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba269-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba269-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba269-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba269-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba269-105">DESCRIPTION</span></span>
<span data-ttu-id="ba269-106">A **Get-AzureRmSqlDatabaseThreatDetectionPolicy** parancsmag egy Azure SQL-adatbázis veszélyforrás-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba269-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="ba269-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paramétert annak az adatbázisnak a meghatározásához, amelyhez a parancsmag a házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="ba269-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="ba269-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ba269-108">EXAMPLES</span></span>

### <span data-ttu-id="ba269-109">Példa 1: az adatbázis veszélyforrás-észlelési házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ba269-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="ba269-110">Ez a parancs a Database01 nevű adatbázis fenyegetés-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba269-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="ba269-111">Az adatbázis a Server01 nevű kiszolgálón található, amelyet az erőforráscsoport ResourceGroup11 társítanak.</span><span class="sxs-lookup"><span data-stu-id="ba269-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ba269-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba269-112">PARAMETERS</span></span>

### <span data-ttu-id="ba269-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba269-113">-DatabaseName</span></span>
<span data-ttu-id="ba269-114">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba269-114">Specifies the name of a database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba269-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba269-115">-DefaultProfile</span></span>
<span data-ttu-id="ba269-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba269-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba269-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba269-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba269-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ba269-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ba269-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ba269-119">-ServerName</span></span>
<span data-ttu-id="ba269-120">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba269-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="ba269-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba269-121">-Confirm</span></span>
<span data-ttu-id="ba269-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba269-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba269-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba269-123">-WhatIf</span></span>
<span data-ttu-id="ba269-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba269-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba269-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba269-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba269-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba269-126">CommonParameters</span></span>
<span data-ttu-id="ba269-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba269-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba269-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba269-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba269-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba269-129">INPUTS</span></span>

###  
<span data-ttu-id="ba269-130">Ebben a parancsmagban nem lehet beírni a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="ba269-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="ba269-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba269-131">OUTPUTS</span></span>

### <span data-ttu-id="ba269-132">Microsoft. Azure. Command. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ba269-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="ba269-133">Ez a parancsmag egy **Model. DatabaseThreatDetectionPolicyModel** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ba269-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="ba269-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba269-134">NOTES</span></span>

## <span data-ttu-id="ba269-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba269-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba269-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba269-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



