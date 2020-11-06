---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: d7fbd87a436b9d0ea2fd0d311e19dc3df5bb8dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499903"
---
# <span data-ttu-id="e0005-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="e0005-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="e0005-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0005-102">SYNOPSIS</span></span>
<span data-ttu-id="e0005-103">Azure Web App-tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="e0005-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0005-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0005-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0005-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0005-105">DESCRIPTION</span></span>
<span data-ttu-id="e0005-106">A **Get-AzureRmWebAppCertificate** parancsmag információkat kap egy adott erőforráscsoport által társított Azure Web App-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="e0005-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="e0005-107">Ha ismeri a tanúsítvány ujjlenyomatát, akkor ezzel a parancsmaggal is információkat kaphat egy adott tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="e0005-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="e0005-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e0005-108">EXAMPLES</span></span>

### <span data-ttu-id="e0005-109">1. példa: webalkalmazás-tanúsítványok beolvasása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="e0005-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e0005-110">Ez a parancs információt ad az erőforráscsoport ContosoResourceGroup társított feltöltött webalkalmazás-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="e0005-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="e0005-111">2. példa: meghatározott webalkalmazási tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0005-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="e0005-112">Ez a parancs a ContosoResourceGroup Web App tanúsítványát az ujjlenyomat E3A38EBA60CAA1C162785A2E1C44A15AD450199C3ja.</span><span class="sxs-lookup"><span data-stu-id="e0005-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="e0005-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0005-113">PARAMETERS</span></span>

### <span data-ttu-id="e0005-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0005-114">-ResourceGroupName</span></span>
<span data-ttu-id="e0005-115">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e0005-115">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0005-116">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="e0005-116">-Thumbprint</span></span>
<span data-ttu-id="e0005-117">A tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0005-117">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0005-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0005-118">-DefaultProfile</span></span>
<span data-ttu-id="e0005-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0005-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0005-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0005-120">CommonParameters</span></span>
<span data-ttu-id="e0005-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0005-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0005-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0005-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0005-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0005-123">INPUTS</span></span>

## <span data-ttu-id="e0005-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0005-124">OUTPUTS</span></span>

## <span data-ttu-id="e0005-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0005-125">NOTES</span></span>

## <span data-ttu-id="e0005-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0005-126">RELATED LINKS</span></span>

[<span data-ttu-id="e0005-127">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e0005-127">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


