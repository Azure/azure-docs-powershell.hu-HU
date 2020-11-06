---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503864"
---
# <span data-ttu-id="4ec01-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ec01-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4ec01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ec01-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec01-103">Módosítja a fiókot.</span><span class="sxs-lookup"><span data-stu-id="4ec01-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ec01-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec01-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ec01-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec01-106">A **set-AzureRmCognitiveServicesAccount** parancsmag a megadott kognitív Services-fiók SKU-ának vagy címkéjének módosítását módosítja.</span><span class="sxs-lookup"><span data-stu-id="4ec01-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="4ec01-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ec01-107">EXAMPLES</span></span>

## <span data-ttu-id="4ec01-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ec01-108">PARAMETERS</span></span>

### <span data-ttu-id="4ec01-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec01-109">-DefaultProfile</span></span>
<span data-ttu-id="4ec01-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ec01-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ec01-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4ec01-111">-Force</span></span>
<span data-ttu-id="4ec01-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4ec01-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ec01-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ec01-113">-Name</span></span>
<span data-ttu-id="4ec01-114">A módosítani kívánt fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ec01-114">Specifies the name of the account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec01-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec01-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ec01-116">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4ec01-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec01-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4ec01-117">-SkuName</span></span>
<span data-ttu-id="4ec01-118">A fiókhoz tartozó SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ec01-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="4ec01-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4ec01-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ec01-120">F0 (ingyenes Tier)</span><span class="sxs-lookup"><span data-stu-id="4ec01-120">F0 (free tier)</span></span>
- <span data-ttu-id="4ec01-121">S0</span><span class="sxs-lookup"><span data-stu-id="4ec01-121">S0</span></span>
- <span data-ttu-id="4ec01-122">S1</span><span class="sxs-lookup"><span data-stu-id="4ec01-122">S1</span></span>
- <span data-ttu-id="4ec01-123">S2</span><span class="sxs-lookup"><span data-stu-id="4ec01-123">S2</span></span>
- <span data-ttu-id="4ec01-124">S3</span><span class="sxs-lookup"><span data-stu-id="4ec01-124">S3</span></span>
- <span data-ttu-id="4ec01-125">S4</span><span class="sxs-lookup"><span data-stu-id="4ec01-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec01-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="4ec01-126">-Tag</span></span>
<span data-ttu-id="4ec01-127">Egy címkét név/érték párokként ad meg.</span><span class="sxs-lookup"><span data-stu-id="4ec01-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec01-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ec01-128">-Confirm</span></span>
<span data-ttu-id="4ec01-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ec01-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec01-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec01-130">-WhatIf</span></span>
<span data-ttu-id="4ec01-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ec01-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec01-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ec01-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec01-133">CommonParameters</span></span>
<span data-ttu-id="4ec01-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ec01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec01-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec01-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec01-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec01-136">INPUTS</span></span>

### <span data-ttu-id="4ec01-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ec01-137">None</span></span>
<span data-ttu-id="4ec01-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4ec01-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ec01-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ec01-139">OUTPUTS</span></span>

### <span data-ttu-id="4ec01-140">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ec01-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4ec01-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ec01-141">NOTES</span></span>

## <span data-ttu-id="4ec01-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ec01-142">RELATED LINKS</span></span>

[<span data-ttu-id="4ec01-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ec01-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4ec01-144">Új – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ec01-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4ec01-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ec01-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
