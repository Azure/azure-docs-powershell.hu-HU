---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: f06075a8067ae8a7d7e1c2dcd522774325b48c57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842789"
---
# <span data-ttu-id="df88f-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="df88f-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="df88f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df88f-102">SYNOPSIS</span></span>
<span data-ttu-id="df88f-103">Azure Web App-tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="df88f-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="df88f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df88f-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df88f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df88f-105">DESCRIPTION</span></span>
<span data-ttu-id="df88f-106">A **Get-AzWebAppCertificate** parancsmag információkat kap egy adott erőforráscsoport által társított Azure Web App-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="df88f-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="df88f-107">Ha ismeri a tanúsítvány ujjlenyomatát, akkor ezzel a parancsmaggal is információkat kaphat egy adott tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="df88f-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="df88f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="df88f-108">EXAMPLES</span></span>

### <span data-ttu-id="df88f-109">1. példa: webalkalmazás-tanúsítványok beolvasása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="df88f-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="df88f-110">Ez a parancs információt ad az erőforráscsoport ContosoResourceGroup társított feltöltött webalkalmazás-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="df88f-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="df88f-111">2. példa: meghatározott webalkalmazási tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="df88f-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="df88f-112">Ez a parancs a ContosoResourceGroup Web App tanúsítványát az ujjlenyomat E3A38EBA60CAA1C162785A2E1C44A15AD450199C3ja.</span><span class="sxs-lookup"><span data-stu-id="df88f-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="df88f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df88f-113">PARAMETERS</span></span>

### <span data-ttu-id="df88f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df88f-114">-DefaultProfile</span></span>
<span data-ttu-id="df88f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df88f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df88f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df88f-116">-ResourceGroupName</span></span>
<span data-ttu-id="df88f-117">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="df88f-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="df88f-118">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="df88f-118">-Thumbprint</span></span>
<span data-ttu-id="df88f-119">A tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="df88f-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="df88f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df88f-120">CommonParameters</span></span>
<span data-ttu-id="df88f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df88f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df88f-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df88f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df88f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df88f-123">INPUTS</span></span>

### <span data-ttu-id="df88f-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="df88f-124">None</span></span>
<span data-ttu-id="df88f-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="df88f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df88f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df88f-126">OUTPUTS</span></span>

## <span data-ttu-id="df88f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df88f-127">NOTES</span></span>

## <span data-ttu-id="df88f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df88f-128">RELATED LINKS</span></span>

[<span data-ttu-id="df88f-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="df88f-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


