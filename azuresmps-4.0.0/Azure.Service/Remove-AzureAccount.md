---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015870"
---
# <span data-ttu-id="d0c5e-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d0c5e-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="d0c5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c5e-103">Azure-fiók törlése a Windows PowerShellből</span><span class="sxs-lookup"><span data-stu-id="d0c5e-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="d0c5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0c5e-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c5e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c5e-106">A **Remove-AzureAccount** parancsmag az Azure-fiókokat és az előfizetéseket az előfizetési adatfájlból törli a központi felhasználói profilból.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="d0c5e-107">A fiók nem törlődik a Microsoft Azure-ból, vagy semmilyen módon nem változtatja meg a tényleges fiókot.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="d0c5e-108">A parancsmag használata nagyon hasonlít az Azure-fiókból való kijelentkezésre.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="d0c5e-109">Ha ismét be szeretne jelentkezni a fiókba, a **Add-AzureAccount** vagy az **import-AzurePublishSettingsFile** segítségével ismét felveheti a fiókot a Windows powershellbe.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="d0c5e-110">A **Remove-AzureAccount** parancsmag használatával megváltoztathatja az Azure PowerShell-parancsmagok Azure-fiókjába való bejelentkezésének módját.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="d0c5e-111">Ha a fiókja mind az **AzurePublishSettingsFile** , mind pedig az Access-jogkivonat felügyeleti tanúsítványát tartalmazza, az Azure PowerShell-parancsmagok csak a hozzáférési jogkivonatot használják, a **AzureAccount**. figyelmen kívül hagyják a kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="d0c5e-112">A felügyeleti tanúsítvány használatához futtassa a **Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="d0c5e-113">Ha a **Remove-AzureAccount** felügyeleti tanúsítványt és hozzáférési jogkivonatot keres, akkor a fiók törlése helyett csak a hozzáférési jogkivonat törlődik.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="d0c5e-114">A felügyeleti tanúsítvány továbbra is fennáll, így a fiók továbbra is elérhető a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="d0c5e-115">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d0c5e-116">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d0c5e-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="d0c5e-117">Példák</span><span class="sxs-lookup"><span data-stu-id="d0c5e-117">EXAMPLES</span></span>

### <span data-ttu-id="d0c5e-118">1. példa: fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d0c5e-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="d0c5e-119">Ez a parancs eltávolítja az admin@contoso.com előfizetési adatfájlból.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="d0c5e-120">Amikor a parancs befejeződött, a fiók már nem érhető el a Windows PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="d0c5e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0c5e-121">PARAMETERS</span></span>

### <span data-ttu-id="d0c5e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d0c5e-122">-Force</span></span>
<span data-ttu-id="d0c5e-123">Letiltja a megerősítési kérdést.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="d0c5e-124">A **Remove-AzureAccount** alapértelmezés szerint a fiók Windows powershellből való eltávolítása előtt kéri.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="d0c5e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0c5e-125">-Name</span></span>
<span data-ttu-id="d0c5e-126">Az eltávolítandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="d0c5e-127">A paraméter értéke megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="d0c5e-128">A helyettesítő karakterek használata nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-128">Wildcard characters are not supported.</span></span>

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

### <span data-ttu-id="d0c5e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0c5e-129">-PassThru</span></span>
<span data-ttu-id="d0c5e-130">A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="d0c5e-131">Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="d0c5e-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="d0c5e-132">-Profile</span></span>
<span data-ttu-id="d0c5e-133">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d0c5e-134">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0c5e-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0c5e-135">-Confirm</span></span>
<span data-ttu-id="d0c5e-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c5e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c5e-137">-WhatIf</span></span>
<span data-ttu-id="d0c5e-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c5e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c5e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c5e-140">CommonParameters</span></span>
<span data-ttu-id="d0c5e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0c5e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c5e-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c5e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c5e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0c5e-143">INPUTS</span></span>

### <span data-ttu-id="d0c5e-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="d0c5e-144">None</span></span>
<span data-ttu-id="d0c5e-145">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d0c5e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0c5e-146">OUTPUTS</span></span>

### <span data-ttu-id="d0c5e-147">Nincs vagy System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0c5e-147">None or System.Boolean</span></span>
<span data-ttu-id="d0c5e-148">Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="d0c5e-149">Ellenkező esetben nem ad vissza semmilyen eredményt.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="d0c5e-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0c5e-150">NOTES</span></span>

## <span data-ttu-id="d0c5e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0c5e-151">RELATED LINKS</span></span>

[<span data-ttu-id="d0c5e-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d0c5e-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="d0c5e-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d0c5e-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


