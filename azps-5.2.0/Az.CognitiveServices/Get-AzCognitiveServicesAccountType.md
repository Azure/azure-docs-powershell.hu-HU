---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338538"
---
# <span data-ttu-id="f52a3-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="f52a3-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="f52a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f52a3-103">A kognitív szolgáltatásokhoz elérhető fióktípusok.</span><span class="sxs-lookup"><span data-stu-id="f52a3-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="f52a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f52a3-104">SYNTAX</span></span>

### <span data-ttu-id="f52a3-105">GetAccountTypes (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f52a3-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f52a3-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="f52a3-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f52a3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f52a3-107">DESCRIPTION</span></span>
<span data-ttu-id="f52a3-108">A **Get-AzCognitiveServicesAccountType** parancsmag az előfizetés alatt elérhető Kognitív szolgáltatások fióktípusokat kapja.</span><span class="sxs-lookup"><span data-stu-id="f52a3-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="f52a3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f52a3-109">EXAMPLES</span></span>

### <span data-ttu-id="f52a3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f52a3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="f52a3-111">Az elérhető típusok listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="f52a3-111">Get the list of available Types.</span></span>

### <span data-ttu-id="f52a3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f52a3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="f52a3-113">Az elérhető típusok listájának lekérte a westus.</span><span class="sxs-lookup"><span data-stu-id="f52a3-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="f52a3-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="f52a3-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="f52a3-115">Ellenőrizze, hogy érvényes-e a típus neve, és ha a név `Face` érvényes név, akkor a visszaadott név lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="f52a3-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="f52a3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f52a3-116">PARAMETERS</span></span>

### <span data-ttu-id="f52a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52a3-117">-DefaultProfile</span></span>
<span data-ttu-id="f52a3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f52a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52a3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f52a3-119">-Location</span></span>
<span data-ttu-id="f52a3-120">Kognitív szolgáltatások fiókjának helye.</span><span class="sxs-lookup"><span data-stu-id="f52a3-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="f52a3-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="f52a3-121">-TypeName</span></span>
<span data-ttu-id="f52a3-122">Kognitív szolgáltatások fióktípusának neve.</span><span class="sxs-lookup"><span data-stu-id="f52a3-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="f52a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52a3-123">CommonParameters</span></span>
<span data-ttu-id="f52a3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52a3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f52a3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52a3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f52a3-126">INPUTS</span></span>

### <span data-ttu-id="f52a3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f52a3-127">System.String</span></span>

## <span data-ttu-id="f52a3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f52a3-128">OUTPUTS</span></span>

### <span data-ttu-id="f52a3-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f52a3-129">System.String[]</span></span>

### <span data-ttu-id="f52a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f52a3-130">System.String</span></span>

## <span data-ttu-id="f52a3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f52a3-131">NOTES</span></span>

## <span data-ttu-id="f52a3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f52a3-132">RELATED LINKS</span></span>
