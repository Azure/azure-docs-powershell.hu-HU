---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 51338a2cae2aa8bde09ecdea18f0aa74f3727fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505223"
---
# <span data-ttu-id="e6f53-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e6f53-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="e6f53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6f53-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f53-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="e6f53-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6f53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6f53-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6f53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6f53-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f53-106">A **set-AzureRmCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="e6f53-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="e6f53-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6f53-107">EXAMPLES</span></span>

## <span data-ttu-id="e6f53-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6f53-108">PARAMETERS</span></span>

### <span data-ttu-id="e6f53-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e6f53-109">-Force</span></span>
<span data-ttu-id="e6f53-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e6f53-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6f53-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6f53-111">-Name</span></span>
<span data-ttu-id="e6f53-112">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6f53-112">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f53-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f53-113">-ResourceGroupName</span></span>
<span data-ttu-id="e6f53-114">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e6f53-114">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="e6f53-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e6f53-115">-SkuName</span></span>
<span data-ttu-id="e6f53-116">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6f53-116">Specifies the SKU for the account.</span></span>
<span data-ttu-id="e6f53-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e6f53-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6f53-118">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="e6f53-118">F0 (free tier)</span></span>
- <span data-ttu-id="e6f53-119">S0</span><span class="sxs-lookup"><span data-stu-id="e6f53-119">S0</span></span>
- <span data-ttu-id="e6f53-120">S1</span><span class="sxs-lookup"><span data-stu-id="e6f53-120">S1</span></span>
- <span data-ttu-id="e6f53-121">S2</span><span class="sxs-lookup"><span data-stu-id="e6f53-121">S2</span></span>
- <span data-ttu-id="e6f53-122">S3</span><span class="sxs-lookup"><span data-stu-id="e6f53-122">S3</span></span>
- <span data-ttu-id="e6f53-123">S4</span><span class="sxs-lookup"><span data-stu-id="e6f53-123">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f53-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="e6f53-124">-Tag</span></span>
<span data-ttu-id="e6f53-125">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="e6f53-125">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f53-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6f53-126">-Confirm</span></span>
<span data-ttu-id="e6f53-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6f53-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f53-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f53-128">-WhatIf</span></span>
<span data-ttu-id="e6f53-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6f53-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f53-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6f53-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f53-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f53-131">-DefaultProfile</span></span>
<span data-ttu-id="e6f53-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6f53-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f53-133">CommonParameters</span></span>
<span data-ttu-id="e6f53-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6f53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f53-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f53-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f53-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6f53-136">INPUTS</span></span>

## <span data-ttu-id="e6f53-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6f53-137">OUTPUTS</span></span>

### <span data-ttu-id="e6f53-138">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e6f53-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="e6f53-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6f53-139">NOTES</span></span>

## <span data-ttu-id="e6f53-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6f53-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6f53-141">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e6f53-141">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e6f53-142">Új – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e6f53-142">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e6f53-143">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e6f53-143">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
