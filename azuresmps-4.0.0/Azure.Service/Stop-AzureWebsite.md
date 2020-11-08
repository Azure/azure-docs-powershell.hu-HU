---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016588"
---
# <span data-ttu-id="893d1-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="893d1-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="893d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="893d1-102">SYNOPSIS</span></span>
<span data-ttu-id="893d1-103">A megadott webhely leállítása.</span><span class="sxs-lookup"><span data-stu-id="893d1-103">Stops the specified website.</span></span>

## <span data-ttu-id="893d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="893d1-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="893d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="893d1-105">DESCRIPTION</span></span>
<span data-ttu-id="893d1-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="893d1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="893d1-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="893d1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="893d1-108">A **stop-AzureWebsite** parancsmag leállítja az Azure-ban üzemeltetett webhelyt.</span><span class="sxs-lookup"><span data-stu-id="893d1-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="893d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="893d1-109">EXAMPLES</span></span>

## <span data-ttu-id="893d1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="893d1-110">PARAMETERS</span></span>

### <span data-ttu-id="893d1-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="893d1-111">-Name</span></span>
<span data-ttu-id="893d1-112">A leállítani kívánt webhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="893d1-112">Specifies the name of the website to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="893d1-113">-PassThru</span></span>
<span data-ttu-id="893d1-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="893d1-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="893d1-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="893d1-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893d1-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="893d1-116">-Profile</span></span>
<span data-ttu-id="893d1-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="893d1-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="893d1-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="893d1-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="893d1-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="893d1-119">-Slot</span></span>
<span data-ttu-id="893d1-120">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="893d1-120">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893d1-121">CommonParameters</span></span>
<span data-ttu-id="893d1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="893d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893d1-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893d1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893d1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="893d1-124">INPUTS</span></span>

## <span data-ttu-id="893d1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="893d1-125">OUTPUTS</span></span>

## <span data-ttu-id="893d1-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="893d1-126">NOTES</span></span>

## <span data-ttu-id="893d1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="893d1-127">RELATED LINKS</span></span>

[<span data-ttu-id="893d1-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="893d1-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="893d1-129">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="893d1-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


