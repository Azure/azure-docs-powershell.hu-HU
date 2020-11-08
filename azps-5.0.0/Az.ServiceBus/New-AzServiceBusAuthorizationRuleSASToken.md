---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195170"
---
# <span data-ttu-id="09843-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="09843-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="09843-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09843-102">SYNOPSIS</span></span>
<span data-ttu-id="09843-103">Létrehoz egy SAS-Tolen az Azure servicebus engedélyezési szabályához a névtér/várólista/témakörben.</span><span class="sxs-lookup"><span data-stu-id="09843-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="09843-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09843-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09843-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09843-105">DESCRIPTION</span></span>
<span data-ttu-id="09843-106">A New-AzServiceBusAuthorizationRuleSASToken parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Eventhub Namesapce vagy az Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="09843-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="09843-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09843-107">EXAMPLES</span></span>

### <span data-ttu-id="09843-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09843-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="09843-109">A megadott authorixation-szabályhoz hozzon létre egy SAS-tokent a Kezdés és a lejárat időpontját tartalmazó névtérhez.</span><span class="sxs-lookup"><span data-stu-id="09843-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="09843-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="09843-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="09843-111">A megadott authorixation-szabályhoz hozzon létre egy SAS-tokent a lejárat időpontját tartalmazó névtérhez.</span><span class="sxs-lookup"><span data-stu-id="09843-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="09843-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09843-112">PARAMETERS</span></span>

### <span data-ttu-id="09843-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="09843-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="09843-114">A Authoraization szabály ResourceId</span><span class="sxs-lookup"><span data-stu-id="09843-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="09843-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09843-115">-DefaultProfile</span></span>
<span data-ttu-id="09843-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09843-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09843-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="09843-117">-ExpiryTime</span></span>
<span data-ttu-id="09843-118">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="09843-118">Expiry Time</span></span>

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

### <span data-ttu-id="09843-119">-Típus</span><span class="sxs-lookup"><span data-stu-id="09843-119">-KeyType</span></span>
<span data-ttu-id="09843-120">Kulcs típusa</span><span class="sxs-lookup"><span data-stu-id="09843-120">Key Type</span></span>

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

### <span data-ttu-id="09843-121">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="09843-121">-StartTime</span></span>
<span data-ttu-id="09843-122">Kezdés időpontja</span><span class="sxs-lookup"><span data-stu-id="09843-122">Start Time</span></span>

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

### <span data-ttu-id="09843-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09843-123">-Confirm</span></span>
<span data-ttu-id="09843-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09843-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09843-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09843-125">-WhatIf</span></span>
<span data-ttu-id="09843-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09843-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09843-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09843-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09843-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09843-128">CommonParameters</span></span>
<span data-ttu-id="09843-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09843-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="09843-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09843-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09843-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09843-131">INPUTS</span></span>

### <span data-ttu-id="09843-132">System. String</span><span class="sxs-lookup"><span data-stu-id="09843-132">System.String</span></span>

### <span data-ttu-id="09843-133">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09843-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="09843-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09843-134">OUTPUTS</span></span>

### <span data-ttu-id="09843-135">Microsoft. Azure. Command. ServiceBus. models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="09843-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="09843-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09843-136">NOTES</span></span>

## <span data-ttu-id="09843-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09843-137">RELATED LINKS</span></span>