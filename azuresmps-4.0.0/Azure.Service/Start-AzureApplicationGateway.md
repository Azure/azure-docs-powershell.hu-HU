---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015779"
---
# <span data-ttu-id="dbb8f-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbb8f-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="dbb8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb8f-103">Elindítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="dbb8f-103">Starts an application gateway.</span></span>

## <span data-ttu-id="dbb8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbb8f-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dbb8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbb8f-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb8f-106">A **Start-AzureApplicationGateway** parancsmag egy alkalmazás-átjárót indít el.</span><span class="sxs-lookup"><span data-stu-id="dbb8f-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="dbb8f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dbb8f-107">EXAMPLES</span></span>

### <span data-ttu-id="dbb8f-108">1. példa: alkalmazás-átjáró indítása</span><span class="sxs-lookup"><span data-stu-id="dbb8f-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="dbb8f-109">Ez a parancs elindítja a ApplicationGateway06 nevű alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="dbb8f-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="dbb8f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbb8f-110">PARAMETERS</span></span>

### <span data-ttu-id="dbb8f-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbb8f-111">-Name</span></span>
<span data-ttu-id="dbb8f-112">Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="dbb8f-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="dbb8f-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="dbb8f-113">-Profile</span></span>
<span data-ttu-id="dbb8f-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dbb8f-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="dbb8f-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dbb8f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dbb8f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb8f-116">CommonParameters</span></span>
<span data-ttu-id="dbb8f-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbb8f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb8f-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb8f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb8f-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbb8f-119">INPUTS</span></span>

### <span data-ttu-id="dbb8f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="dbb8f-120">System.String</span></span>

## <span data-ttu-id="dbb8f-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbb8f-121">OUTPUTS</span></span>

### <span data-ttu-id="dbb8f-122">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dbb8f-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="dbb8f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbb8f-123">NOTES</span></span>

## <span data-ttu-id="dbb8f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbb8f-124">RELATED LINKS</span></span>

[<span data-ttu-id="dbb8f-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbb8f-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="dbb8f-126">Új – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbb8f-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="dbb8f-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbb8f-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="dbb8f-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbb8f-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="dbb8f-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbb8f-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


