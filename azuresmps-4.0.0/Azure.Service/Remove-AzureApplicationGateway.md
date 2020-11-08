---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016497"
---
# <span data-ttu-id="1d62d-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d62d-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="1d62d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d62d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d62d-103">Egy alkalmazás átjárójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1d62d-103">Removes an application gateway.</span></span>

## <span data-ttu-id="1d62d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d62d-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1d62d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d62d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d62d-106">A **Remove-AzureApplicationGateway** parancsmag eltávolítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="1d62d-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="1d62d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1d62d-107">EXAMPLES</span></span>

### <span data-ttu-id="1d62d-108">1. példa: az alkalmazás-átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1d62d-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="1d62d-109">Ez a parancs eltávolítja a ApplicationGateway06 nevű alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="1d62d-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="1d62d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d62d-110">PARAMETERS</span></span>

### <span data-ttu-id="1d62d-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d62d-111">-Name</span></span>
<span data-ttu-id="1d62d-112">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1d62d-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1d62d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="1d62d-113">-Profile</span></span>
<span data-ttu-id="1d62d-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1d62d-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1d62d-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1d62d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d62d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d62d-116">CommonParameters</span></span>
<span data-ttu-id="1d62d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d62d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d62d-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d62d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d62d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d62d-119">INPUTS</span></span>

### <span data-ttu-id="1d62d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="1d62d-120">System.String</span></span>

## <span data-ttu-id="1d62d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d62d-121">OUTPUTS</span></span>

### <span data-ttu-id="1d62d-122">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1d62d-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="1d62d-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d62d-123">NOTES</span></span>

## <span data-ttu-id="1d62d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d62d-124">RELATED LINKS</span></span>

[<span data-ttu-id="1d62d-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d62d-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="1d62d-126">Új – AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d62d-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="1d62d-127">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d62d-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="1d62d-128">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d62d-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="1d62d-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d62d-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


