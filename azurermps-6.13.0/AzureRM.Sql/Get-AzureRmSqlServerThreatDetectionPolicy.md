---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: d6e9ac96a5263add451fb03eae7783fe344852fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492726"
---
# <span data-ttu-id="5510b-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5510b-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="5510b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5510b-102">SYNOPSIS</span></span>
<span data-ttu-id="5510b-103">A kiszolgáló veszélyforrás-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5510b-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5510b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5510b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5510b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5510b-105">DESCRIPTION</span></span>
<span data-ttu-id="5510b-106">A **Get-AzureRmSqlServerThreatDetectionPolicy** parancsmag az Azure SQL Server fenyegetések észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5510b-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="5510b-107">A parancsmag használatához adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert annak a kiszolgálónak a meghatározásához, amelynek a parancsmagja a házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="5510b-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="5510b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5510b-108">EXAMPLES</span></span>

### <span data-ttu-id="5510b-109">Példa 1: a fenyegetések észlelési házirendjének beszerzése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="5510b-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="5510b-110">Ez a parancs a Server01 nevű kiszolgáló fenyegetés-észlelési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5510b-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="5510b-111">A kiszolgáló az erőforráscsoport ResourceGroup11 van társítva.</span><span class="sxs-lookup"><span data-stu-id="5510b-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="5510b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5510b-112">PARAMETERS</span></span>

### <span data-ttu-id="5510b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5510b-113">-DefaultProfile</span></span>
<span data-ttu-id="5510b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5510b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5510b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5510b-115">-ResourceGroupName</span></span>
<span data-ttu-id="5510b-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="5510b-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="5510b-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5510b-117">-ServerName</span></span>
<span data-ttu-id="5510b-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5510b-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5510b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5510b-119">-Confirm</span></span>
<span data-ttu-id="5510b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5510b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5510b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5510b-121">-WhatIf</span></span>
<span data-ttu-id="5510b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5510b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5510b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5510b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5510b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5510b-124">CommonParameters</span></span>
<span data-ttu-id="5510b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5510b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5510b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5510b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5510b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5510b-127">INPUTS</span></span>

### <span data-ttu-id="5510b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5510b-128">System.String</span></span>

## <span data-ttu-id="5510b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5510b-129">OUTPUTS</span></span>

### <span data-ttu-id="5510b-130">Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5510b-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="5510b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5510b-131">NOTES</span></span>

## <span data-ttu-id="5510b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5510b-132">RELATED LINKS</span></span>

[<span data-ttu-id="5510b-133">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5510b-133">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="5510b-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5510b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


