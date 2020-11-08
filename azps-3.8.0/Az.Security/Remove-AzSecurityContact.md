---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: ed4afca4d422245be721c7b50d45ecaab45b5c81
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011584"
---
# <span data-ttu-id="29769-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="29769-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="29769-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29769-102">SYNOPSIS</span></span>
<span data-ttu-id="29769-103">Biztonsági névjegykártya törlése</span><span class="sxs-lookup"><span data-stu-id="29769-103">Deletes a security contact.</span></span>

## <span data-ttu-id="29769-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29769-104">SYNTAX</span></span>

### <span data-ttu-id="29769-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29769-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29769-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29769-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29769-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="29769-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29769-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="29769-108">DESCRIPTION</span></span>
<span data-ttu-id="29769-109">Biztonsági névjegykártya törlése</span><span class="sxs-lookup"><span data-stu-id="29769-109">Deletes a security contact.</span></span>

## <span data-ttu-id="29769-110">Példák</span><span class="sxs-lookup"><span data-stu-id="29769-110">EXAMPLES</span></span>

### <span data-ttu-id="29769-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29769-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="29769-112">A "default1" biztonsági névjegykártya törlése</span><span class="sxs-lookup"><span data-stu-id="29769-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="29769-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29769-113">PARAMETERS</span></span>

### <span data-ttu-id="29769-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29769-114">-DefaultProfile</span></span>
<span data-ttu-id="29769-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29769-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29769-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29769-116">-InputObject</span></span>
<span data-ttu-id="29769-117">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="29769-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29769-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29769-118">-Name</span></span>
<span data-ttu-id="29769-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="29769-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29769-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29769-120">-PassThru</span></span>
<span data-ttu-id="29769-121">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="29769-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="29769-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29769-122">-ResourceId</span></span>
<span data-ttu-id="29769-123">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="29769-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29769-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29769-124">-Confirm</span></span>
<span data-ttu-id="29769-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29769-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29769-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29769-126">-WhatIf</span></span>
<span data-ttu-id="29769-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29769-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29769-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29769-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29769-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29769-129">CommonParameters</span></span>
<span data-ttu-id="29769-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29769-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29769-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29769-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29769-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29769-132">INPUTS</span></span>

### <span data-ttu-id="29769-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29769-133">System.String</span></span>

### <span data-ttu-id="29769-134">Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="29769-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="29769-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29769-135">OUTPUTS</span></span>

### <span data-ttu-id="29769-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29769-136">System.Boolean</span></span>

## <span data-ttu-id="29769-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29769-137">NOTES</span></span>

## <span data-ttu-id="29769-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29769-138">RELATED LINKS</span></span>
