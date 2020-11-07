---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: a1064b42a5d30dde5ba51f3333ef1e4836ed7159
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666483"
---
# <span data-ttu-id="01418-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="01418-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="01418-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01418-102">SYNOPSIS</span></span>
<span data-ttu-id="01418-103">Létrehoz egy SAS-Tolen az Azure eventhub engedélyezési szabályához a Namespace/eventhub.</span><span class="sxs-lookup"><span data-stu-id="01418-103">Generates a SAS tolen for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="01418-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01418-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01418-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01418-105">DESCRIPTION</span></span>
<span data-ttu-id="01418-106">A New-AzEventHubAuthorizationRuleSASToken parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Eventhub Namesapce vagy az Azure Eventhub</span><span class="sxs-lookup"><span data-stu-id="01418-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="01418-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01418-107">EXAMPLES</span></span>

### <span data-ttu-id="01418-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="01418-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="01418-109">A megadott authorixation-szabályhoz hozzon létre egy SAS-tokent a Kezdés és a lejárat időpontját tartalmazó névtérhez.</span><span class="sxs-lookup"><span data-stu-id="01418-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="01418-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="01418-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="01418-111">A megadott authorixation-szabályhoz hozzon létre egy SAS-tokent a lejárat időpontját tartalmazó névtérhez.</span><span class="sxs-lookup"><span data-stu-id="01418-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="01418-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01418-112">PARAMETERS</span></span>

### <span data-ttu-id="01418-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="01418-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="01418-114">A Authoraization szabály ResourceId</span><span class="sxs-lookup"><span data-stu-id="01418-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="01418-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01418-115">-DefaultProfile</span></span>
<span data-ttu-id="01418-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01418-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01418-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="01418-117">-ExpiryTime</span></span>
<span data-ttu-id="01418-118">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="01418-118">Expiry Time</span></span>

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

### <span data-ttu-id="01418-119">-Típus</span><span class="sxs-lookup"><span data-stu-id="01418-119">-KeyType</span></span>
<span data-ttu-id="01418-120">Kulcs típusa</span><span class="sxs-lookup"><span data-stu-id="01418-120">Key Type</span></span>

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

### <span data-ttu-id="01418-121">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="01418-121">-StartTime</span></span>
<span data-ttu-id="01418-122">Kezdés időpontja</span><span class="sxs-lookup"><span data-stu-id="01418-122">Start Time</span></span>

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

### <span data-ttu-id="01418-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01418-123">-Confirm</span></span>
<span data-ttu-id="01418-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01418-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01418-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01418-125">-WhatIf</span></span>
<span data-ttu-id="01418-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01418-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01418-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01418-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01418-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01418-128">CommonParameters</span></span>
<span data-ttu-id="01418-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01418-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="01418-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01418-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01418-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01418-131">INPUTS</span></span>

### <span data-ttu-id="01418-132">System. String</span><span class="sxs-lookup"><span data-stu-id="01418-132">System.String</span></span>

### <span data-ttu-id="01418-133">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="01418-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="01418-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01418-134">OUTPUTS</span></span>

### <span data-ttu-id="01418-135">Microsoft. Azure. Command. EventHub. models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="01418-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="01418-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01418-136">NOTES</span></span>

## <span data-ttu-id="01418-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01418-137">RELATED LINKS</span></span>
