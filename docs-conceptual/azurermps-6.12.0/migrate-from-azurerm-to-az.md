---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg a szkriptek az AzureRM modulból az új Az modulba való áttelepítésére szolgáló lépéseket és eszközöket.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574413"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="8d111-103">Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba</span><span class="sxs-lookup"><span data-stu-id="8d111-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="8d111-104">Az Az modul a funkciók tekintetében paritásban van az AzureRM modullal, de rövidebb és egységesebb parancsmagneveket használ.</span><span class="sxs-lookup"><span data-stu-id="8d111-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="8d111-105">Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az új modullal.</span><span class="sxs-lookup"><span data-stu-id="8d111-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="8d111-106">Az áttérés megkönnyítése érdekében az Az olyan eszközöket nyújt, amelyekkel futtathatja az AzureRM-et használó meglévő szkripteket.</span><span class="sxs-lookup"><span data-stu-id="8d111-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="8d111-107">Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az új modulra való átállás alapjaival.</span><span class="sxs-lookup"><span data-stu-id="8d111-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="8d111-108">Gondoskodjon róla, hogy a meglévő szkriptek működjenek az AzureRM legfrissebb kiadásával.</span><span class="sxs-lookup"><span data-stu-id="8d111-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="8d111-109">Ez az a legfontosabb lépés!</span><span class="sxs-lookup"><span data-stu-id="8d111-109">This is the most important step!</span></span> <span data-ttu-id="8d111-110">Futtassa a meglévő szkriptjeit, és ellenőrizze, hogy működnek-e az AzureRM _legfrissebb_ kiadásával (__6.12.0__).</span><span class="sxs-lookup"><span data-stu-id="8d111-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.12.0__).</span></span> <span data-ttu-id="8d111-111">Ha a szkriptek nem működnek, tekintse át [az AzureRM áttelepítési útmutatóját](migration-guide.6.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="8d111-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="8d111-112">Az Azure PowerShell Az modul telepítése</span><span class="sxs-lookup"><span data-stu-id="8d111-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="8d111-113">Az első lépés az Az modul telepítése a platformra.</span><span class="sxs-lookup"><span data-stu-id="8d111-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="8d111-114">Az Az telepítéséhez el kell távolítania az AzureRM-et.</span><span class="sxs-lookup"><span data-stu-id="8d111-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="8d111-115">A következő lépésekben bemutatjuk, hogyan futtathatja továbbra is meglévő szkriptjeit, és hogyan biztosíthatja a régi parancsmagnevek kompatibilitását.</span><span class="sxs-lookup"><span data-stu-id="8d111-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="8d111-116">Az Azure PowerShell Az modul telepítéséhez hajtsa végre az alábbi lépéseket:</span><span class="sxs-lookup"><span data-stu-id="8d111-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="8d111-117">[Az AzureRM modul eltávolítása](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="8d111-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="8d111-118">Győződjön meg róla, hogy az AzureRM _összes_ telepített verzióját eltávolítja, és nem csak a legutóbbi verziót.</span><span class="sxs-lookup"><span data-stu-id="8d111-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="8d111-119">Az Az modul telepítése</span><span class="sxs-lookup"><span data-stu-id="8d111-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="8d111-120"><a name="aliases"/>Az AzureRM alias módjának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8d111-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="8d111-121">Miután az AzureRM-et eltávolította, és megbizonyosodott róla, hogy a szkriptek működnek az AzureRM legfrissebb verziójával, ideje engedélyeznie az Az modul kompatibilitási módját.</span><span class="sxs-lookup"><span data-stu-id="8d111-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="8d111-122">A kompatibilitás a következő paranccsal engedélyezhető:</span><span class="sxs-lookup"><span data-stu-id="8d111-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="8d111-123">Az aliasok segítségével továbbra is használhatja a régi parancsmagneveket, ha az `Az` modul van telepítve.</span><span class="sxs-lookup"><span data-stu-id="8d111-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="8d111-124">Az aliasokat a kiválasztott hatókör felhasználói profiljába lesznek írva.</span><span class="sxs-lookup"><span data-stu-id="8d111-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="8d111-125">Ha nincs felhasználói profil, a rendszer létrehoz egyet.</span><span class="sxs-lookup"><span data-stu-id="8d111-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="8d111-126">Használhat más hatókört (`-Scope`) is a parancsban, ez azonban nem ajánlott!</span><span class="sxs-lookup"><span data-stu-id="8d111-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="8d111-127">Ezek az aliasok a kiválasztott hatókör felhasználói profiljába lesznek írva, ezért érdemes őket minél korlátozottabb hatókörhöz engedélyezni.</span><span class="sxs-lookup"><span data-stu-id="8d111-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="8d111-128">Az aliasok rendszerszintű engedélyezése emellett a többi felhasználónak is problémát okozhat, akiknél az `AzureRM` van telepítve a helyi hatókörükben.</span><span class="sxs-lookup"><span data-stu-id="8d111-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="8d111-129">Az alias mód engedélyezése után futtassa újra a szkripteket, és győződjön meg róla, hogy továbbra is a vártnak megfelelően működnek.</span><span class="sxs-lookup"><span data-stu-id="8d111-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="8d111-130">A modulimportálások és parancsmagnevek módosítása</span><span class="sxs-lookup"><span data-stu-id="8d111-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="8d111-131">Általánosságban véve a modulnevek módosultak, így az `AzureRM` és az `Azure` is `Az` lett, és ugyanez igaz a parancsmagokra is.</span><span class="sxs-lookup"><span data-stu-id="8d111-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="8d111-132">Az `AzureRM.Compute` modul új neve például `Az.Compute`.</span><span class="sxs-lookup"><span data-stu-id="8d111-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="8d111-133">A `New-AzureRmVM` `New-AzVM` lett, a `Get-AzureStorageBlob` pedig `Get-AzStorageBlob`.</span><span class="sxs-lookup"><span data-stu-id="8d111-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="8d111-134">Van néhány kivétel is ez alól a szabály alól, amelyeket érdemes figyelembe venni, mielőtt bármit átnevezne:</span><span class="sxs-lookup"><span data-stu-id="8d111-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="8d111-135">AzureRM modul</span><span class="sxs-lookup"><span data-stu-id="8d111-135">AzureRM module</span></span> | <span data-ttu-id="8d111-136">Az modul</span><span class="sxs-lookup"><span data-stu-id="8d111-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="8d111-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="8d111-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="8d111-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d111-138">Az.DataFactory</span></span> |
| <span data-ttu-id="8d111-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d111-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="8d111-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d111-140">Az.DataFactory</span></span> |
| <span data-ttu-id="8d111-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d111-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="8d111-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d111-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="8d111-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8d111-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="8d111-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d111-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="8d111-145">Összegzés</span><span class="sxs-lookup"><span data-stu-id="8d111-145">Summary</span></span>

<span data-ttu-id="8d111-146">Ezeknek a lépéseknek a végrehajtásával frissítheti az összes meglévő szkriptet az új modul használatára.</span><span class="sxs-lookup"><span data-stu-id="8d111-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="8d111-147">Amennyiben az áttelepítést során valamelyik lépéssel kapcsolatban kérdés vagy probléma merült fel, amely megnehezítette a dolgát, várjuk a megjegyzéseit a cikk alatt, hogy fejleszthessük az útmutatót.</span><span class="sxs-lookup"><span data-stu-id="8d111-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>