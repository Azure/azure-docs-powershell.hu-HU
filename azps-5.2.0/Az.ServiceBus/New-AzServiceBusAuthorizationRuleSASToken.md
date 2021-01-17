---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371250"
---
# <span data-ttu-id="e2524-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e2524-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="e2524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2524-102">SYNOPSIS</span></span>
<span data-ttu-id="e2524-103">A névtér/várólista/témakör Azure servicebus-engedélyezési szabályának SAS-tolen-ét generálja.</span><span class="sxs-lookup"><span data-stu-id="e2524-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="e2524-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2524-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2524-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2524-105">DESCRIPTION</span></span>
<span data-ttu-id="e2524-106">A New-AzServiceBusAuthorizationRuleSASToken parancsmag létrehoz egy SAS-jogkivonatot egy Azure Eventhub Namesapce vagy Azure Eventhub eseményhubhoz</span><span class="sxs-lookup"><span data-stu-id="e2524-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="e2524-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2524-107">EXAMPLES</span></span>

### <span data-ttu-id="e2524-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2524-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="e2524-109">Hozzon létre SAS-jogkivonatot a Namespace-hez kezdési és lejárati idővel érvényes szerzői jogkivonathoz.</span><span class="sxs-lookup"><span data-stu-id="e2524-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="e2524-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="e2524-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="e2524-111">Hozzon létre SAS-jogkivonatot a névtérhez érvényes érvényesítési idővel érvényes szerzői jogkivonathoz.</span><span class="sxs-lookup"><span data-stu-id="e2524-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="e2524-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2524-112">PARAMETERS</span></span>

### <span data-ttu-id="e2524-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="e2524-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="e2524-114">ARM szerzői jog szabály ResourceId-jének létrehozása</span><span class="sxs-lookup"><span data-stu-id="e2524-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="e2524-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2524-115">-DefaultProfile</span></span>
<span data-ttu-id="e2524-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2524-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2524-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e2524-117">-ExpiryTime</span></span>
<span data-ttu-id="e2524-118">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="e2524-118">Expiry Time</span></span>

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

### <span data-ttu-id="e2524-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e2524-119">-KeyType</span></span>
<span data-ttu-id="e2524-120">Billentyű típusa</span><span class="sxs-lookup"><span data-stu-id="e2524-120">Key Type</span></span>

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

### <span data-ttu-id="e2524-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e2524-121">-StartTime</span></span>
<span data-ttu-id="e2524-122">Kezdési időpont</span><span class="sxs-lookup"><span data-stu-id="e2524-122">Start Time</span></span>

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

### <span data-ttu-id="e2524-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2524-123">-Confirm</span></span>
<span data-ttu-id="e2524-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e2524-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2524-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2524-125">-WhatIf</span></span>
<span data-ttu-id="e2524-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e2524-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2524-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2524-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2524-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2524-128">CommonParameters</span></span>
<span data-ttu-id="e2524-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2524-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e2524-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2524-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2524-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2524-131">INPUTS</span></span>

### <span data-ttu-id="e2524-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e2524-132">System.String</span></span>

### <span data-ttu-id="e2524-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e2524-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e2524-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2524-134">OUTPUTS</span></span>

### <span data-ttu-id="e2524-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="e2524-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="e2524-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2524-136">NOTES</span></span>

## <span data-ttu-id="e2524-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2524-137">RELATED LINKS</span></span>