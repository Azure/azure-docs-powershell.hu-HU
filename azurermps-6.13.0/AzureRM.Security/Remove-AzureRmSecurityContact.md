---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501071"
---
# <span data-ttu-id="517c9-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="517c9-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="517c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="517c9-102">SYNOPSIS</span></span>
<span data-ttu-id="517c9-103">Biztonsági névjegykártya törlése</span><span class="sxs-lookup"><span data-stu-id="517c9-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="517c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="517c9-104">SYNTAX</span></span>

### <span data-ttu-id="517c9-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="517c9-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517c9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="517c9-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517c9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="517c9-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="517c9-108">DESCRIPTION</span></span>
<span data-ttu-id="517c9-109">Biztonsági névjegykártya törlése</span><span class="sxs-lookup"><span data-stu-id="517c9-109">Deletes a security contact.</span></span>

## <span data-ttu-id="517c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="517c9-110">EXAMPLES</span></span>

### <span data-ttu-id="517c9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="517c9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="517c9-112">A "default1" biztonsági névjegykártya törlése</span><span class="sxs-lookup"><span data-stu-id="517c9-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="517c9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="517c9-113">PARAMETERS</span></span>

### <span data-ttu-id="517c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517c9-114">-DefaultProfile</span></span>
<span data-ttu-id="517c9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="517c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517c9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="517c9-116">-InputObject</span></span>
<span data-ttu-id="517c9-117">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="517c9-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="517c9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="517c9-118">-Name</span></span>
<span data-ttu-id="517c9-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="517c9-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517c9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="517c9-120">-PassThru</span></span>
<span data-ttu-id="517c9-121">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="517c9-121">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="517c9-122">-ResourceId</span></span>
<span data-ttu-id="517c9-123">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="517c9-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="517c9-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="517c9-124">-Confirm</span></span>
<span data-ttu-id="517c9-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="517c9-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517c9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517c9-126">-WhatIf</span></span>
<span data-ttu-id="517c9-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="517c9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="517c9-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="517c9-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517c9-129">CommonParameters</span></span>
<span data-ttu-id="517c9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="517c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517c9-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517c9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517c9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="517c9-132">INPUTS</span></span>

### <span data-ttu-id="517c9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="517c9-133">System.String</span></span>
<span data-ttu-id="517c9-134">Microsoft. Azure. Command. Security. parancsmagok. SecurityContacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="517c9-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="517c9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="517c9-135">OUTPUTS</span></span>

### <span data-ttu-id="517c9-136">Microsoft. Azure. commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="517c9-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="517c9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="517c9-137">NOTES</span></span>

## <span data-ttu-id="517c9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="517c9-138">RELATED LINKS</span></span>
