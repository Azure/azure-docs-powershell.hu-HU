---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016020"
---
# <span data-ttu-id="a4618-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="a4618-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="a4618-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4618-102">SYNOPSIS</span></span>
<span data-ttu-id="a4618-103">Azure RemoteApp program közzétételének visszavonása</span><span class="sxs-lookup"><span data-stu-id="a4618-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="a4618-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4618-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4618-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4618-105">DESCRIPTION</span></span>
<span data-ttu-id="a4618-106">A Közzététel visszavonása **– AzureRemoteAppProgram** parancsmag visszavonja az Azure RemoteApp program közzétételét.</span><span class="sxs-lookup"><span data-stu-id="a4618-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="a4618-107">A program közzétételének megszüntetése után már nem érhető el az Azure RemoteApp-gyűjtemény felhasználói.</span><span class="sxs-lookup"><span data-stu-id="a4618-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a4618-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a4618-108">EXAMPLES</span></span>

## <span data-ttu-id="a4618-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4618-109">PARAMETERS</span></span>

### <span data-ttu-id="a4618-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="a4618-110">-Alias</span></span>
<span data-ttu-id="a4618-111">Itt adhatja meg, hogy a programok milyen aliasokat tegyenek közzé.</span><span class="sxs-lookup"><span data-stu-id="a4618-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="a4618-112">A **Get-AzureRemoteAppProgram** használatával lekérdezheti a program aliasát a közzététel visszavonásához.</span><span class="sxs-lookup"><span data-stu-id="a4618-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4618-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a4618-113">-CollectionName</span></span>
<span data-ttu-id="a4618-114">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4618-114">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4618-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="a4618-115">-Profile</span></span>
<span data-ttu-id="a4618-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="a4618-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4618-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="a4618-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4618-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4618-118">-Confirm</span></span>
<span data-ttu-id="a4618-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4618-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4618-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4618-120">-WhatIf</span></span>
<span data-ttu-id="a4618-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4618-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4618-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4618-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4618-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4618-123">CommonParameters</span></span>
<span data-ttu-id="a4618-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4618-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4618-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4618-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4618-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4618-126">INPUTS</span></span>

## <span data-ttu-id="a4618-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4618-127">OUTPUTS</span></span>

## <span data-ttu-id="a4618-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4618-128">NOTES</span></span>

## <span data-ttu-id="a4618-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4618-129">RELATED LINKS</span></span>

[<span data-ttu-id="a4618-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="a4618-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="a4618-131">Közzététel – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="a4618-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


