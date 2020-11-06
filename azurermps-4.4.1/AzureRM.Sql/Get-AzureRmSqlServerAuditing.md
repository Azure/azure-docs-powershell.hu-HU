---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495532"
---
# <span data-ttu-id="8f0a6-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="8f0a6-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="8f0a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0a6-103">Egy Azure SQL Server naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f0a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f0a6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f0a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8f0a6-106">A **Get-AzureRmSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók blob-naplózási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="8f0a6-107">Adja meg a *ResourceGroupName* és a *kiszolgálónév* paramétert az adatbázis azonosítójának megadásához.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="8f0a6-108">Ez a parancsmag a megadott Azure SQL-kiszolgálón definiált Azure SQL-adatbázisok által használt házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="8f0a6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8f0a6-109">EXAMPLES</span></span>

### <span data-ttu-id="8f0a6-110">1. példa: az Azure SQL Server naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="8f0a6-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="8f0a6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f0a6-111">PARAMETERS</span></span>

### <span data-ttu-id="8f0a6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f0a6-112">-ResourceGroupName</span></span>
<span data-ttu-id="8f0a6-113">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f0a6-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8f0a6-114">-ServerName</span></span>
<span data-ttu-id="8f0a6-115">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-115">SQL server name.</span></span>

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

### <span data-ttu-id="8f0a6-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f0a6-116">-Confirm</span></span>
<span data-ttu-id="8f0a6-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f0a6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f0a6-118">-WhatIf</span></span>
<span data-ttu-id="8f0a6-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f0a6-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f0a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0a6-121">-DefaultProfile</span></span>
<span data-ttu-id="8f0a6-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f0a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0a6-123">CommonParameters</span></span>
<span data-ttu-id="8f0a6-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f0a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0a6-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f0a6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0a6-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f0a6-126">INPUTS</span></span>

## <span data-ttu-id="8f0a6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f0a6-127">OUTPUTS</span></span>

### <span data-ttu-id="8f0a6-128">Microsoft. Azure. Command. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="8f0a6-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="8f0a6-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f0a6-129">NOTES</span></span>

## <span data-ttu-id="8f0a6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f0a6-130">RELATED LINKS</span></span>

