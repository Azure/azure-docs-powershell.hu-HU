---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016322"
---
# <span data-ttu-id="91c9a-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="91c9a-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="91c9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="91c9a-103">Beolvassa az Azure RemoteApp művelet eredményét.</span><span class="sxs-lookup"><span data-stu-id="91c9a-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="91c9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91c9a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91c9a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="91c9a-106">A **Get-AzureRemoteAppOperationResult** parancsmag beolvassa az Azure-alapú, hosszú ideig futó Azure-RemoteApp műveletek eredményét.</span><span class="sxs-lookup"><span data-stu-id="91c9a-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="91c9a-107">Az Azure RemoteApp hosszú futású műveleteket végez sok olyan műveletnél, amely a szolgáltatás általi feldolgozást igényel, és nem tud azonnal visszaadni.</span><span class="sxs-lookup"><span data-stu-id="91c9a-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="91c9a-108">Példák a nyomkövetési azonosítókat tartalmazó parancsmagokra: **Update-AzureRemoteAppCollection** , **set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** és egyebek.</span><span class="sxs-lookup"><span data-stu-id="91c9a-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="91c9a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="91c9a-109">EXAMPLES</span></span>

### <span data-ttu-id="91c9a-110">1. példa: a nyomkövetési azonosító használata a műveleti eredmény eléréséhez</span><span class="sxs-lookup"><span data-stu-id="91c9a-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="91c9a-111">Ez a parancs az Azure RemoteApp műveletből visszaadott nyomkövetési azonosítót menti.</span><span class="sxs-lookup"><span data-stu-id="91c9a-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="91c9a-112">A rendszer átadja a nyomkövetési azonosítót a **Get-AzureRemoteAppOperationResult** az alábbi parancsban.</span><span class="sxs-lookup"><span data-stu-id="91c9a-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="91c9a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91c9a-113">PARAMETERS</span></span>

### <span data-ttu-id="91c9a-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="91c9a-114">-Profile</span></span>
<span data-ttu-id="91c9a-115">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="91c9a-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91c9a-116">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="91c9a-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91c9a-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="91c9a-117">-TrackingId</span></span>
<span data-ttu-id="91c9a-118">Egy művelet nyomkövetési AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91c9a-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c9a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c9a-119">CommonParameters</span></span>
<span data-ttu-id="91c9a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91c9a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c9a-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c9a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c9a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c9a-122">INPUTS</span></span>

## <span data-ttu-id="91c9a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c9a-123">OUTPUTS</span></span>

## <span data-ttu-id="91c9a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91c9a-124">NOTES</span></span>

## <span data-ttu-id="91c9a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91c9a-125">RELATED LINKS</span></span>

[<span data-ttu-id="91c9a-126">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="91c9a-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="91c9a-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="91c9a-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="91c9a-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="91c9a-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


