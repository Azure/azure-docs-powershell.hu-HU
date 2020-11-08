---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016030"
---
# <span data-ttu-id="a696b-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="a696b-101">Start-AzureService</span></span>

## <span data-ttu-id="a696b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a696b-102">SYNOPSIS</span></span>
<span data-ttu-id="a696b-103">A megadott hosztolt szolgáltatás elindítása a Windows Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="a696b-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="a696b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a696b-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a696b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a696b-105">DESCRIPTION</span></span>
<span data-ttu-id="a696b-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="a696b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a696b-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a696b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a696b-108">A **Start-AzureService** parancsmag a megadott hosztolt szolgáltatást a Windows Azure-ban indítja el, ha a szolgáltatás leállított állapotban van.</span><span class="sxs-lookup"><span data-stu-id="a696b-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="a696b-109">Felhívjuk a figyelmét arra, hogy a **közzétételi AzureServiceProject** parancsmag automatikusan megkísérli elindítani a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a696b-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="a696b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a696b-110">EXAMPLES</span></span>

## <span data-ttu-id="a696b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a696b-111">PARAMETERS</span></span>

### <span data-ttu-id="a696b-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a696b-112">-PassThru</span></span>
<span data-ttu-id="a696b-113">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a696b-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a696b-114">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a696b-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a696b-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="a696b-115">-Profile</span></span>
<span data-ttu-id="a696b-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a696b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a696b-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a696b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a696b-118">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a696b-118">-ServiceName</span></span>
<span data-ttu-id="a696b-119">A elindítani kívánt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a696b-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="a696b-120">Ha nincs megadva név, a parancsmag elindítja az aktuálisan hosztolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a696b-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="a696b-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a696b-121">-Slot</span></span>
<span data-ttu-id="a696b-122">Azt a telepítési bővítőhelyet adja meg, amelyben a szolgáltatás indítását vagy gyártását szeretné elindítani.</span><span class="sxs-lookup"><span data-stu-id="a696b-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="a696b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a696b-123">CommonParameters</span></span>
<span data-ttu-id="a696b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a696b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a696b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a696b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a696b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a696b-126">INPUTS</span></span>

## <span data-ttu-id="a696b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a696b-127">OUTPUTS</span></span>

## <span data-ttu-id="a696b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a696b-128">NOTES</span></span>

## <span data-ttu-id="a696b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a696b-129">RELATED LINKS</span></span>

[<span data-ttu-id="a696b-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="a696b-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="a696b-131">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="a696b-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="a696b-132">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="a696b-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


