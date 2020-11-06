---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495268"
---
# <span data-ttu-id="ec61f-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ec61f-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="ec61f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec61f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec61f-103">Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="ec61f-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec61f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec61f-104">SYNTAX</span></span>

### <span data-ttu-id="ec61f-105">ApplicationObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec61f-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec61f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec61f-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec61f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec61f-107">DESCRIPTION</span></span>
<span data-ttu-id="ec61f-108">Az Get-AzureRmADAppCredential parancsmag használatával lekérheti az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="ec61f-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="ec61f-109">Ez a parancs az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja kikeresni.</span><span class="sxs-lookup"><span data-stu-id="ec61f-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="ec61f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ec61f-110">EXAMPLES</span></span>

### <span data-ttu-id="ec61f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec61f-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="ec61f-112">A "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektummal társított hitelesítő adatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ec61f-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="ec61f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec61f-113">PARAMETERS</span></span>

### <span data-ttu-id="ec61f-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ec61f-114">-ApplicationId</span></span>
<span data-ttu-id="ec61f-115">Az alkalmazás azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="ec61f-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec61f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec61f-116">-DefaultProfile</span></span>
<span data-ttu-id="ec61f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ec61f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec61f-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec61f-118">-ObjectId</span></span>
<span data-ttu-id="ec61f-119">A hitelesítő adatok beolvasására szolgáló alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec61f-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec61f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec61f-120">CommonParameters</span></span>
<span data-ttu-id="ec61f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec61f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec61f-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec61f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec61f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec61f-123">INPUTS</span></span>

### <span data-ttu-id="ec61f-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec61f-124">None</span></span>
<span data-ttu-id="ec61f-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ec61f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec61f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec61f-126">OUTPUTS</span></span>

### <span data-ttu-id="ec61f-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ec61f-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ec61f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec61f-128">NOTES</span></span>

## <span data-ttu-id="ec61f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec61f-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec61f-130">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ec61f-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="ec61f-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ec61f-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="ec61f-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ec61f-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

