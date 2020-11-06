---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: e2aaa6ed6e66e61f8d62f1235ff8e2a8ff9f65e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492966"
---
# <span data-ttu-id="60c7f-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="60c7f-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="60c7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="60c7f-103">Azure Web App-tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="60c7f-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60c7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60c7f-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c7f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="60c7f-106">A **Get-AzureRmWebAppCertificate** parancsmag információkat kap egy adott erőforráscsoport által társított Azure Web App-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="60c7f-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="60c7f-107">Ha ismeri a tanúsítvány ujjlenyomatát, akkor ezzel a parancsmaggal is információkat kaphat egy adott tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="60c7f-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="60c7f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="60c7f-108">EXAMPLES</span></span>

### <span data-ttu-id="60c7f-109">1. példa: webalkalmazás-tanúsítványok beolvasása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="60c7f-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="60c7f-110">Ez a parancs információt ad az erőforráscsoport ContosoResourceGroup társított feltöltött webalkalmazás-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="60c7f-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="60c7f-111">2. példa: meghatározott webalkalmazási tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="60c7f-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="60c7f-112">Ez a parancs a ContosoResourceGroup Web App tanúsítványát az ujjlenyomat E3A38EBA60CAA1C162785A2E1C44A15AD450199C3ja.</span><span class="sxs-lookup"><span data-stu-id="60c7f-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="60c7f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60c7f-113">PARAMETERS</span></span>

### <span data-ttu-id="60c7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c7f-114">-DefaultProfile</span></span>
<span data-ttu-id="60c7f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60c7f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60c7f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c7f-116">-ResourceGroupName</span></span>
<span data-ttu-id="60c7f-117">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="60c7f-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c7f-118">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="60c7f-118">-Thumbprint</span></span>
<span data-ttu-id="60c7f-119">A tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="60c7f-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c7f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c7f-120">CommonParameters</span></span>
<span data-ttu-id="60c7f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60c7f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c7f-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c7f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c7f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60c7f-123">INPUTS</span></span>

### <span data-ttu-id="60c7f-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="60c7f-124">None</span></span>
<span data-ttu-id="60c7f-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="60c7f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60c7f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60c7f-126">OUTPUTS</span></span>

## <span data-ttu-id="60c7f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60c7f-127">NOTES</span></span>

## <span data-ttu-id="60c7f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60c7f-128">RELATED LINKS</span></span>

[<span data-ttu-id="60c7f-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="60c7f-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


