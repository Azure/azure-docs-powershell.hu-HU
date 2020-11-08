---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016477"
---
# <span data-ttu-id="4fe55-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4fe55-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="4fe55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fe55-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe55-103">Azure-környezet törlése a Windows PowerShellből</span><span class="sxs-lookup"><span data-stu-id="4fe55-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="4fe55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fe55-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4fe55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fe55-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe55-106">A **Remove-AzureEnvironment** parancsmag egy Azure-környezetet töröl a központi profilból, így a Windows PowerShell nem találja.</span><span class="sxs-lookup"><span data-stu-id="4fe55-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="4fe55-107">Ez a parancsmag nem törli a környezetet a Microsoft Azure rendszerből, illetve semmilyen módon nem változtatja meg a tényleges környezetet.</span><span class="sxs-lookup"><span data-stu-id="4fe55-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="4fe55-108">Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.</span><span class="sxs-lookup"><span data-stu-id="4fe55-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="4fe55-109">A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.</span><span class="sxs-lookup"><span data-stu-id="4fe55-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="4fe55-110">További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4fe55-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="4fe55-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4fe55-111">EXAMPLES</span></span>

### <span data-ttu-id="4fe55-112">Példa 1: környezet törlése</span><span class="sxs-lookup"><span data-stu-id="4fe55-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="4fe55-113">Ez a parancs törli a ContosoEnv-környezetet a Windows PowerShellből.</span><span class="sxs-lookup"><span data-stu-id="4fe55-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="4fe55-114">2. példa: több környezet törlése</span><span class="sxs-lookup"><span data-stu-id="4fe55-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="4fe55-115">Ez a parancs törli azokat a környezeteket, amelyek neve "contoso" néven kezdődik a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="4fe55-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="4fe55-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fe55-116">PARAMETERS</span></span>

### <span data-ttu-id="4fe55-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4fe55-117">-Force</span></span>
<span data-ttu-id="4fe55-118">Letiltja a megerősítési kérdést.</span><span class="sxs-lookup"><span data-stu-id="4fe55-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="4fe55-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fe55-119">-Name</span></span>
<span data-ttu-id="4fe55-120">Az eltávolítandó környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fe55-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="4fe55-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fe55-121">This parameter is required.</span></span>
<span data-ttu-id="4fe55-122">Ez a paraméterérték megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="4fe55-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="4fe55-123">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="4fe55-123">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="4fe55-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="4fe55-124">-Profile</span></span>
<span data-ttu-id="4fe55-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4fe55-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4fe55-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4fe55-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4fe55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe55-127">CommonParameters</span></span>
<span data-ttu-id="4fe55-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fe55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe55-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe55-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe55-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fe55-130">INPUTS</span></span>

### <span data-ttu-id="4fe55-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="4fe55-131">None</span></span>
<span data-ttu-id="4fe55-132">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="4fe55-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4fe55-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fe55-133">OUTPUTS</span></span>

### <span data-ttu-id="4fe55-134">Nincs vagy System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe55-134">None or System.Boolean</span></span>
<span data-ttu-id="4fe55-135">Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4fe55-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="4fe55-136">Ellenkező esetben nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="4fe55-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="4fe55-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fe55-137">NOTES</span></span>

## <span data-ttu-id="4fe55-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fe55-138">RELATED LINKS</span></span>

[<span data-ttu-id="4fe55-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4fe55-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="4fe55-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4fe55-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="4fe55-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4fe55-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


