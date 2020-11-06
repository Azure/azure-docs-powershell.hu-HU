---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504768"
---
# <span data-ttu-id="7330d-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7330d-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="7330d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7330d-102">SYNOPSIS</span></span>
<span data-ttu-id="7330d-103">Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="7330d-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7330d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7330d-104">SYNTAX</span></span>

### <span data-ttu-id="7330d-105">ApplicationObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7330d-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7330d-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7330d-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7330d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7330d-107">DESCRIPTION</span></span>
<span data-ttu-id="7330d-108">Az Get-AzureRmADAppCredential parancsmag használatával lekérheti az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="7330d-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="7330d-109">Ez a parancs az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja kikeresni.</span><span class="sxs-lookup"><span data-stu-id="7330d-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="7330d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7330d-110">EXAMPLES</span></span>

### <span data-ttu-id="7330d-111">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7330d-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="7330d-112">A "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektummal társított hitelesítő adatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7330d-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="7330d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7330d-113">PARAMETERS</span></span>

### <span data-ttu-id="7330d-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7330d-114">-ApplicationId</span></span>
<span data-ttu-id="7330d-115">Az alkalmazás azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="7330d-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7330d-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7330d-116">-ObjectId</span></span>
<span data-ttu-id="7330d-117">A hitelesítő adatok beolvasására szolgáló alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7330d-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7330d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7330d-118">-DefaultProfile</span></span>
<span data-ttu-id="7330d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7330d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7330d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7330d-120">CommonParameters</span></span>
<span data-ttu-id="7330d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7330d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7330d-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7330d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7330d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7330d-123">INPUTS</span></span>

## <span data-ttu-id="7330d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7330d-124">OUTPUTS</span></span>

### <span data-ttu-id="7330d-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7330d-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="7330d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7330d-126">NOTES</span></span>

## <span data-ttu-id="7330d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7330d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7330d-128">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7330d-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7330d-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7330d-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="7330d-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7330d-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

