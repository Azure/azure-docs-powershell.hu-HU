---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015838"
---
# <span data-ttu-id="4e57f-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4e57f-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="4e57f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e57f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e57f-103">Webfeladatot állít be egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="4e57f-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="4e57f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e57f-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e57f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e57f-105">DESCRIPTION</span></span>
<span data-ttu-id="4e57f-106">A **stop-AzureWebsiteJob** parancsmag leállítja a webhelyek webfeladatát.</span><span class="sxs-lookup"><span data-stu-id="4e57f-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="4e57f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e57f-107">EXAMPLES</span></span>

### <span data-ttu-id="4e57f-108">Példa 1: webfeladat leállítása a webhelyen</span><span class="sxs-lookup"><span data-stu-id="4e57f-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="4e57f-109">Leállítja a MyWebJob nevű webes feladatot a MyWebSite.</span><span class="sxs-lookup"><span data-stu-id="4e57f-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="4e57f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e57f-110">PARAMETERS</span></span>

### <span data-ttu-id="4e57f-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="4e57f-111">-JobName</span></span>
<span data-ttu-id="4e57f-112">A webes feladat neve.</span><span class="sxs-lookup"><span data-stu-id="4e57f-112">The web job name.</span></span>

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

### <span data-ttu-id="4e57f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e57f-113">-Name</span></span>
<span data-ttu-id="4e57f-114">Az Azure-webhely neve.</span><span class="sxs-lookup"><span data-stu-id="4e57f-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="4e57f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e57f-115">-PassThru</span></span>
<span data-ttu-id="4e57f-116">Egy logikai értéket ad eredményül, amely azt jelzi, hogy a feladat sikeresen leállt.</span><span class="sxs-lookup"><span data-stu-id="4e57f-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="4e57f-117">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="4e57f-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="4e57f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="4e57f-118">-Profile</span></span>
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

### <span data-ttu-id="4e57f-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="4e57f-119">-Slot</span></span>
<span data-ttu-id="4e57f-120">Az Azure-webhely tárolóhelyének neve.</span><span class="sxs-lookup"><span data-stu-id="4e57f-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="4e57f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e57f-121">CommonParameters</span></span>
<span data-ttu-id="4e57f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e57f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e57f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e57f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e57f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e57f-124">INPUTS</span></span>

## <span data-ttu-id="4e57f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e57f-125">OUTPUTS</span></span>

## <span data-ttu-id="4e57f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e57f-126">NOTES</span></span>

## <span data-ttu-id="4e57f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e57f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e57f-128">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4e57f-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="4e57f-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4e57f-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="4e57f-130">Új – AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4e57f-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="4e57f-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4e57f-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="4e57f-132">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4e57f-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


