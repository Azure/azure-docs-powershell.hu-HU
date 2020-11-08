---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013733"
---
# <span data-ttu-id="ec630-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ec630-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="ec630-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec630-102">SYNOPSIS</span></span>
<span data-ttu-id="ec630-103">Létrehoz egy SAS-Tolen az Azure servicebus engedélyezési szabályához a névtér/várólista/témakörben.</span><span class="sxs-lookup"><span data-stu-id="ec630-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="ec630-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec630-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec630-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec630-105">DESCRIPTION</span></span>
<span data-ttu-id="ec630-106">A New-AzServiceBusAuthorizationRuleSASToken parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Eventhub Namesapce vagy az Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="ec630-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="ec630-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec630-107">EXAMPLES</span></span>

### <span data-ttu-id="ec630-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec630-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="ec630-109">A megadott authorixation-szabályhoz hozzon létre egy SAS-tokent a Kezdés és a lejárat időpontját tartalmazó névtérhez.</span><span class="sxs-lookup"><span data-stu-id="ec630-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="ec630-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="ec630-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="ec630-111">A megadott authorixation-szabályhoz hozzon létre egy SAS-tokent a lejárat időpontját tartalmazó névtérhez.</span><span class="sxs-lookup"><span data-stu-id="ec630-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="ec630-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec630-112">PARAMETERS</span></span>

### <span data-ttu-id="ec630-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="ec630-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="ec630-114">A Authoraization szabály ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec630-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec630-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec630-115">-DefaultProfile</span></span>
<span data-ttu-id="ec630-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec630-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec630-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ec630-117">-ExpiryTime</span></span>
<span data-ttu-id="ec630-118">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="ec630-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec630-119">-Típus</span><span class="sxs-lookup"><span data-stu-id="ec630-119">-KeyType</span></span>
<span data-ttu-id="ec630-120">Kulcs típusa</span><span class="sxs-lookup"><span data-stu-id="ec630-120">Key Type</span></span>

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

### <span data-ttu-id="ec630-121">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="ec630-121">-StartTime</span></span>
<span data-ttu-id="ec630-122">Kezdés időpontja</span><span class="sxs-lookup"><span data-stu-id="ec630-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec630-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec630-123">-Confirm</span></span>
<span data-ttu-id="ec630-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec630-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec630-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec630-125">-WhatIf</span></span>
<span data-ttu-id="ec630-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec630-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec630-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec630-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec630-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec630-128">CommonParameters</span></span>
<span data-ttu-id="ec630-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec630-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ec630-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec630-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec630-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec630-131">INPUTS</span></span>

### <span data-ttu-id="ec630-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ec630-132">System.String</span></span>

### <span data-ttu-id="ec630-133">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ec630-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ec630-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec630-134">OUTPUTS</span></span>

### <span data-ttu-id="ec630-135">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="ec630-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="ec630-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec630-136">NOTES</span></span>

## <span data-ttu-id="ec630-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec630-137">RELATED LINKS</span></span>