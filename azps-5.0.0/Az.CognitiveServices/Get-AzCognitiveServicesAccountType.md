---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300374"
---
# <span data-ttu-id="c9c5a-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="c9c5a-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="c9c5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c5a-103">Megkapja a rendelkezésre álló kognitív szolgáltatások számlatípust.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="c9c5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9c5a-104">SYNTAX</span></span>

### <span data-ttu-id="c9c5a-105">GetAccountTypes (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9c5a-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c5a-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="c9c5a-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9c5a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c5a-108">A **Get-AzCognitiveServicesAccountType** parancsmag a rendelkezésre álló kognitív Services típusú fiókokat az előfizetés alatt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="c9c5a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c9c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="c9c5a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9c5a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="c9c5a-111">A rendelkezésre álló típusok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c9c5a-111">Get the list of available Types.</span></span>

### <span data-ttu-id="c9c5a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9c5a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="c9c5a-113">A rendelkezésre álló típusok listájának beszerzése a westus.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="c9c5a-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9c5a-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="c9c5a-115">Ellenőrizze, hogy érvényes-e a név `Face` , a nevet a program visszaadja, ha az érvényes név.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="c9c5a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9c5a-116">PARAMETERS</span></span>

### <span data-ttu-id="c9c5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c5a-117">-DefaultProfile</span></span>
<span data-ttu-id="c9c5a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c5a-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="c9c5a-119">-Location</span></span>
<span data-ttu-id="c9c5a-120">A kognitív szolgáltatások fiók helye.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="c9c5a-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="c9c5a-121">-TypeName</span></span>
<span data-ttu-id="c9c5a-122">A kognitív szolgáltatások fiók típusa név.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="c9c5a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c5a-123">CommonParameters</span></span>
<span data-ttu-id="c9c5a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9c5a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c5a-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9c5a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c5a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c5a-126">INPUTS</span></span>

### <span data-ttu-id="c9c5a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c5a-127">System.String</span></span>

## <span data-ttu-id="c9c5a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9c5a-128">OUTPUTS</span></span>

### <span data-ttu-id="c9c5a-129">System. string []</span><span class="sxs-lookup"><span data-stu-id="c9c5a-129">System.String[]</span></span>

### <span data-ttu-id="c9c5a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c5a-130">System.String</span></span>

## <span data-ttu-id="c9c5a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9c5a-131">NOTES</span></span>

## <span data-ttu-id="c9c5a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9c5a-132">RELATED LINKS</span></span>
