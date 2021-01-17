---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467033"
---
# <span data-ttu-id="7f809-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="7f809-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="7f809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f809-102">SYNOPSIS</span></span>
<span data-ttu-id="7f809-103">Azure Web App-tanúsítványt kap.</span><span class="sxs-lookup"><span data-stu-id="7f809-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="7f809-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f809-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f809-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f809-105">DESCRIPTION</span></span>
<span data-ttu-id="7f809-106">A **Get-AzWebAppCertificate** parancsmag információt kap egy adott erőforráscsoporthoz társított Azure Web App-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="7f809-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="7f809-107">Ha tudja a tanúsítvány thumbprint, akkor is használhatja ezt a parancsmagot, hogy információkat kap egy adott tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="7f809-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="7f809-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f809-108">EXAMPLES</span></span>

### <span data-ttu-id="7f809-109">1. példa: Webalkalmazás-tanúsítványok lekérte egy erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="7f809-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7f809-110">Ez a parancs információkat ad vissza a ContosoResourceGroup erőforráscsoporthoz társított feltöltött webalkalmazás-tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="7f809-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="7f809-111">2. példa: Megadott webalkalmazás-tanúsítvány letöltése</span><span class="sxs-lookup"><span data-stu-id="7f809-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="7f809-112">Ez a parancs az E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 hüvelykujjat is mutató ContosoResourceGroup Web App tanúsítványt kapja.</span><span class="sxs-lookup"><span data-stu-id="7f809-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="7f809-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f809-113">PARAMETERS</span></span>

### <span data-ttu-id="7f809-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f809-114">-DefaultProfile</span></span>
<span data-ttu-id="7f809-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f809-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f809-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f809-116">-ResourceGroupName</span></span>
<span data-ttu-id="7f809-117">Annak az erőforráscsoportnak a neve, amelyhez a tanúsítvány hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="7f809-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="7f809-118">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="7f809-118">-Thumbprint</span></span>
<span data-ttu-id="7f809-119">A tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f809-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="7f809-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f809-120">CommonParameters</span></span>
<span data-ttu-id="7f809-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f809-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f809-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f809-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f809-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f809-123">INPUTS</span></span>

### <span data-ttu-id="7f809-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="7f809-124">None</span></span>

## <span data-ttu-id="7f809-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f809-125">OUTPUTS</span></span>

### <span data-ttu-id="7f809-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="7f809-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="7f809-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f809-127">NOTES</span></span>

## <span data-ttu-id="7f809-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f809-128">RELATED LINKS</span></span>

[<span data-ttu-id="7f809-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7f809-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


