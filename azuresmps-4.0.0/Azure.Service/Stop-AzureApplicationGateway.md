---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016408"
---
# <span data-ttu-id="c0c1a-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0c1a-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="c0c1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c1a-103">Egy alkalmazás átjárójának leállítása</span><span class="sxs-lookup"><span data-stu-id="c0c1a-103">Stops an application gateway.</span></span>

## <span data-ttu-id="c0c1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0c1a-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c0c1a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c1a-106">A **stop-AzureApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="c0c1a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c0c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c1a-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="c0c1a-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="c0c1a-109">Ez a parancs leállítja a ApplicationGateway06 nevű alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="c0c1a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0c1a-110">PARAMETERS</span></span>

### <span data-ttu-id="c0c1a-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0c1a-111">-Name</span></span>
<span data-ttu-id="c0c1a-112">Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c1a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="c0c1a-113">-Profile</span></span>
<span data-ttu-id="c0c1a-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0c1a-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c0c1a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c1a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c1a-116">CommonParameters</span></span>
<span data-ttu-id="c0c1a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0c1a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c1a-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c1a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c1a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c1a-119">INPUTS</span></span>

### <span data-ttu-id="c0c1a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c0c1a-120">System.String</span></span>

## <span data-ttu-id="c0c1a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c1a-121">OUTPUTS</span></span>

### <span data-ttu-id="c0c1a-122">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c0c1a-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="c0c1a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0c1a-123">NOTES</span></span>

## <span data-ttu-id="c0c1a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0c1a-124">RELATED LINKS</span></span>

[<span data-ttu-id="c0c1a-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0c1a-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="c0c1a-126">Új – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0c1a-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="c0c1a-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0c1a-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="c0c1a-128">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0c1a-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="c0c1a-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0c1a-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
