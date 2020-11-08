---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016084"
---
# <span data-ttu-id="67f58-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="67f58-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="67f58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67f58-102">SYNOPSIS</span></span>
<span data-ttu-id="67f58-103">Egy virtuális gép újraindítása az Azure RemoteApp-gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="67f58-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="67f58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67f58-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67f58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67f58-105">DESCRIPTION</span></span>
<span data-ttu-id="67f58-106">Az **Újraindítás – AzureRemoteAppVM** parancsmag egy virtuális gépet egy olyan Azure RemoteApp-gyűjteményből indít újra, amelyen az adott felhasználó csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="67f58-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="67f58-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67f58-107">EXAMPLES</span></span>

### <span data-ttu-id="67f58-108">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="67f58-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="67f58-109">Ez a parancs a contoso nevű Azure RemoteApp-gyűjteményben egy virtuális gépet újraindul.</span><span class="sxs-lookup"><span data-stu-id="67f58-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="67f58-110">A felhasználó PattiFuller@contoso.com csatlakozik a virtuális gépet tartalmazó gyűjteményhez.</span><span class="sxs-lookup"><span data-stu-id="67f58-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="67f58-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67f58-111">PARAMETERS</span></span>

### <span data-ttu-id="67f58-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="67f58-112">-CollectionName</span></span>
<span data-ttu-id="67f58-113">Egy Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67f58-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f58-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="67f58-114">-LogoffMessage</span></span>
<span data-ttu-id="67f58-115">A virtuális géphez kapcsolt felhasználók számára figyelmeztető üzenetet jelenít meg, mielőtt a parancsmag kijelentkezik.</span><span class="sxs-lookup"><span data-stu-id="67f58-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67f58-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="67f58-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="67f58-117">Itt adhatja meg, hogy a parancsmag mennyi ideig várjon, mielőtt a felhasználók bejelentkeznek.</span><span class="sxs-lookup"><span data-stu-id="67f58-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="67f58-118">Az alapértelmezett érték 60 másodperc.</span><span class="sxs-lookup"><span data-stu-id="67f58-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67f58-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="67f58-119">-Profile</span></span>
<span data-ttu-id="67f58-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="67f58-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67f58-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="67f58-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67f58-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="67f58-122">-UserUpn</span></span>
<span data-ttu-id="67f58-123">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek a parancsmagja a virtuális gépet újraindította.</span><span class="sxs-lookup"><span data-stu-id="67f58-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="67f58-124">Ha virtuális gépeket szeretne beolvasni a gyűjteményben és a csatlakoztatott UPN-ben, használja a **Get-AzureRemoteAppVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="67f58-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67f58-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67f58-125">-Confirm</span></span>
<span data-ttu-id="67f58-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67f58-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f58-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67f58-127">-WhatIf</span></span>
<span data-ttu-id="67f58-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67f58-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f58-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67f58-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f58-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f58-130">CommonParameters</span></span>
<span data-ttu-id="67f58-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67f58-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f58-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f58-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f58-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f58-133">INPUTS</span></span>

## <span data-ttu-id="67f58-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f58-134">OUTPUTS</span></span>

## <span data-ttu-id="67f58-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67f58-135">NOTES</span></span>

## <span data-ttu-id="67f58-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67f58-136">RELATED LINKS</span></span>

[<span data-ttu-id="67f58-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="67f58-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


