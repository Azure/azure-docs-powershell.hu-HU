---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332298"
---
# <span data-ttu-id="07ca4-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="07ca4-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="07ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="07ca4-103">Egy SAS-jogkivonatot hoz létre a namespace/eventhub azure eventhub engedélyezési szabálya számára.</span><span class="sxs-lookup"><span data-stu-id="07ca4-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="07ca4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07ca4-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07ca4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="07ca4-106">A New-AzEventHubAuthorizationRuleSASToken parancsmag létrehoz egy SAS-jogkivonatot egy Azure Eventhub Namesapce vagy Azure Eventhub eseményhubhoz</span><span class="sxs-lookup"><span data-stu-id="07ca4-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="07ca4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07ca4-107">EXAMPLES</span></span>

### <span data-ttu-id="07ca4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="07ca4-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="07ca4-109">Hozzon létre SAS-jogkivonatot a Namespace-hez kezdési és lejárati idővel érvényes szerzői jogkivonathoz.</span><span class="sxs-lookup"><span data-stu-id="07ca4-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="07ca4-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="07ca4-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="07ca4-111">Hozzon létre SAS-jogkivonatot a névtérhez érvényes érvényesítési idővel érvényes szerzői jogkivonathoz.</span><span class="sxs-lookup"><span data-stu-id="07ca4-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="07ca4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07ca4-112">PARAMETERS</span></span>

### <span data-ttu-id="07ca4-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="07ca4-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="07ca4-114">ARM szerzői jog szabály ResourceId-jének létrehozása</span><span class="sxs-lookup"><span data-stu-id="07ca4-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="07ca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ca4-115">-DefaultProfile</span></span>
<span data-ttu-id="07ca4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07ca4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ca4-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="07ca4-117">-ExpiryTime</span></span>
<span data-ttu-id="07ca4-118">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="07ca4-118">Expiry Time</span></span>

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

### <span data-ttu-id="07ca4-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="07ca4-119">-KeyType</span></span>
<span data-ttu-id="07ca4-120">Billentyű típusa</span><span class="sxs-lookup"><span data-stu-id="07ca4-120">Key Type</span></span>

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

### <span data-ttu-id="07ca4-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="07ca4-121">-StartTime</span></span>
<span data-ttu-id="07ca4-122">Kezdési időpont</span><span class="sxs-lookup"><span data-stu-id="07ca4-122">Start Time</span></span>

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

### <span data-ttu-id="07ca4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07ca4-123">-Confirm</span></span>
<span data-ttu-id="07ca4-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07ca4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ca4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ca4-125">-WhatIf</span></span>
<span data-ttu-id="07ca4-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07ca4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ca4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07ca4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ca4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ca4-128">CommonParameters</span></span>
<span data-ttu-id="07ca4-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ca4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="07ca4-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ca4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ca4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07ca4-131">INPUTS</span></span>

### <span data-ttu-id="07ca4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="07ca4-132">System.String</span></span>

### <span data-ttu-id="07ca4-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="07ca4-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="07ca4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07ca4-134">OUTPUTS</span></span>

### <span data-ttu-id="07ca4-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="07ca4-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="07ca4-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07ca4-136">NOTES</span></span>

## <span data-ttu-id="07ca4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07ca4-137">RELATED LINKS</span></span>
