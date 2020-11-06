---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501172"
---
# <span data-ttu-id="92519-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="92519-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="92519-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92519-102">SYNOPSIS</span></span>
<span data-ttu-id="92519-103">Megkapja a rendelkezésre álló kognitív szolgáltatások számlatípust.</span><span class="sxs-lookup"><span data-stu-id="92519-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92519-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92519-104">SYNTAX</span></span>

### <span data-ttu-id="92519-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="92519-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92519-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="92519-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92519-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92519-107">DESCRIPTION</span></span>
<span data-ttu-id="92519-108">A **Get-AzureRmCognitiveServicesAccountType** parancsmag a rendelkezésre álló kognitív Services típusú fiókokat az előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="92519-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="92519-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92519-109">EXAMPLES</span></span>

### <span data-ttu-id="92519-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92519-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="92519-111">A rendelkezésre álló típusok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="92519-111">Get the list of available Types.</span></span>

### <span data-ttu-id="92519-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="92519-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="92519-113">A rendelkezésre álló típusok listájának beszerzése a westus.</span><span class="sxs-lookup"><span data-stu-id="92519-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="92519-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="92519-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="92519-115">Ellenőrizze, hogy érvényes-e a név `Face` , a nevet a program visszaadja, ha az érvényes név.</span><span class="sxs-lookup"><span data-stu-id="92519-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="92519-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92519-116">PARAMETERS</span></span>

### <span data-ttu-id="92519-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92519-117">-DefaultProfile</span></span>
<span data-ttu-id="92519-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92519-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92519-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="92519-119">-Location</span></span>
<span data-ttu-id="92519-120">A kognitív szolgáltatások fiók helye.</span><span class="sxs-lookup"><span data-stu-id="92519-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92519-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="92519-121">-TypeName</span></span>
<span data-ttu-id="92519-122">A kognitív szolgáltatások fiók típusa név.</span><span class="sxs-lookup"><span data-stu-id="92519-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92519-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92519-123">CommonParameters</span></span>
<span data-ttu-id="92519-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92519-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92519-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92519-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92519-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92519-126">INPUTS</span></span>

### <span data-ttu-id="92519-127">System. String</span><span class="sxs-lookup"><span data-stu-id="92519-127">System.String</span></span>

## <span data-ttu-id="92519-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92519-128">OUTPUTS</span></span>

### <span data-ttu-id="92519-129">System. string []</span><span class="sxs-lookup"><span data-stu-id="92519-129">System.String[]</span></span>

### <span data-ttu-id="92519-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92519-130">System.String</span></span>

## <span data-ttu-id="92519-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92519-131">NOTES</span></span>

## <span data-ttu-id="92519-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92519-132">RELATED LINKS</span></span>
