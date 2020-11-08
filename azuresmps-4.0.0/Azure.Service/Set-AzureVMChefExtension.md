---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016045"
---
# <span data-ttu-id="3a9e7-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3a9e7-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="3a9e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9e7-103">Hozzáadja a séf bővítményt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="3a9e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a9e7-104">SYNTAX</span></span>

### <span data-ttu-id="3a9e7-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a9e7-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a9e7-106">Linux</span><span class="sxs-lookup"><span data-stu-id="3a9e7-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3a9e7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a9e7-107">DESCRIPTION</span></span>
<span data-ttu-id="3a9e7-108">A **set-AzureVMChefExtension** parancsmag hozzáadja a Chef bővítményt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="3a9e7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3a9e7-109">EXAMPLES</span></span>

### <span data-ttu-id="3a9e7-110">1. példa: Chef-kiterjesztés hozzáadása Windows Virtual Machine-géphez</span><span class="sxs-lookup"><span data-stu-id="3a9e7-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="3a9e7-111">A parancs hozzáadja a Chef bővítményt a Windows Virtual Machine programhoz.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="3a9e7-112">Amikor a virtuális gép jön létre, a bootstrapped a séf, és az Apache-ot futtatja.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="3a9e7-113">2. példa: a Chef Extension bővítmény felvétele Windows Virtual Machine-be a rendszerindítás során</span><span class="sxs-lookup"><span data-stu-id="3a9e7-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="3a9e7-114">Ez a parancs hozzáadja a Chef bővítményt egy Windows Virtual Machine programhoz.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="3a9e7-115">Amikor elindul a virtuális gép, a bootstrapped a séf futtatja, és az Apache-ot futtatja.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="3a9e7-116">A rendszerindítás után a virtuális gép a JSON formátumban megadott *BootstrapOptions* hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="3a9e7-117">3. példa: Chef-kiterjesztés felvétele Windows Virtual Machine-be, és telepítése az Apache és a GIT segítségével</span><span class="sxs-lookup"><span data-stu-id="3a9e7-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="3a9e7-118">Ez a parancs hozzáadja a Chef bővítményt egy Windows Virtual Machine programhoz.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="3a9e7-119">Amikor elindul a virtuális gép, bootstrapped a séf, és telepítve van az Apache és a GIT.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="3a9e7-120">Ha nem adja meg az Client. RB, meg kell adni a séf-kiszolgáló URL-címét és az érvényesítési ügyfél nevét.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="3a9e7-121">4. példa: Chef-kiterjesztés hozzáadása egy linuxos virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="3a9e7-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="3a9e7-122">Ez a parancs hozzáadja a Chef bővítményt egy linuxos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="3a9e7-123">Amikor elindul a virtuális gép, az a séf bootstrapped van.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="3a9e7-124">Ha nem ad meg ügyfelet. RB, meg kell adni a séf-kiszolgáló URL-címét és szervezetét.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="3a9e7-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a9e7-125">PARAMETERS</span></span>

### <span data-ttu-id="3a9e7-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="3a9e7-126">-BootstrapOptions</span></span>
<span data-ttu-id="3a9e7-127">A betöltési beállításokat a JavaScript-objektumokhoz (JSON) tartalmazó formátumban adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="3a9e7-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="3a9e7-128">-BootstrapVersion</span></span>
<span data-ttu-id="3a9e7-129">A Chef ügyfélprogramnak a kiterjesztéssel együtt telepített verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="3a9e7-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="3a9e7-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="3a9e7-131">Annak gyakoriságát adja meg (percben), amikor a séf-szolgáltatás fut.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="3a9e7-132">Ha abban az esetben, ha nem szeretné, hogy a séf-szolgáltatás telepítve legyen az Azure VM-ben, akkor ebben a mezőben a 0 értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e7-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="3a9e7-133">-ChefServerUrl</span></span>
<span data-ttu-id="3a9e7-134">A séf-kiszolgáló URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="3a9e7-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="3a9e7-135">-ClientRb</span></span>
<span data-ttu-id="3a9e7-136">A Chef Client. RB teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="3a9e7-137">-Daemon</span><span class="sxs-lookup"><span data-stu-id="3a9e7-137">-Daemon</span></span>
<span data-ttu-id="3a9e7-138">A Chef-Client szolgáltatás beállítása felügyelet nélküli végrehajtáshoz.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="3a9e7-139">A csomópont platformjának Windows rendszernek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-139">The node platform should be Windows.</span></span>
<span data-ttu-id="3a9e7-140">Engedélyezett beállítások: "nincs", "szolgáltatás" és "tevékenység".</span><span class="sxs-lookup"><span data-stu-id="3a9e7-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="3a9e7-141">nincs – ez a beállítás megakadályozza a Chef-Client szolgáltatás szolgáltatásként való konfigurálását.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="3a9e7-142">szolgáltatás – beállítja a séf – ügyfelet, hogy szolgáltatásként automatikusan fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="3a9e7-143">feladat – úgy állítja be a Chef-clientt, hogy automatikusan fusson a háttérben secheduled tevékenységként.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="3a9e7-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3a9e7-144">-InformationAction</span></span>
<span data-ttu-id="3a9e7-145">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3a9e7-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3a9e7-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a9e7-147">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3a9e7-147">Continue</span></span>
- <span data-ttu-id="3a9e7-148">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3a9e7-148">Ignore</span></span>
- <span data-ttu-id="3a9e7-149">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3a9e7-149">Inquire</span></span>
- <span data-ttu-id="3a9e7-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3a9e7-150">SilentlyContinue</span></span>
- <span data-ttu-id="3a9e7-151">állj</span><span class="sxs-lookup"><span data-stu-id="3a9e7-151">Stop</span></span>
- <span data-ttu-id="3a9e7-152">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3a9e7-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e7-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3a9e7-153">-InformationVariable</span></span>
<span data-ttu-id="3a9e7-154">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e7-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="3a9e7-155">-JsonAttribute</span></span>
<span data-ttu-id="3a9e7-156">A Chef-Client első futtatásához hozzáadni kívánt JSON-karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="3a9e7-157">például-JsonAttribute ' {"foo": "sáv"} '</span><span class="sxs-lookup"><span data-stu-id="3a9e7-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="3a9e7-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="3a9e7-158">-Linux</span></span>
<span data-ttu-id="3a9e7-159">Jelzi, hogy ez a parancsmag egy Linux-beli virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e7-160">-Szervezetnév</span><span class="sxs-lookup"><span data-stu-id="3a9e7-160">-OrganizationName</span></span>
<span data-ttu-id="3a9e7-161">A séf-kiterjesztés szervezeti nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="3a9e7-162">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a9e7-162">-Profile</span></span>
<span data-ttu-id="3a9e7-163">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a9e7-164">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a9e7-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="3a9e7-165">-RunList</span></span>
<span data-ttu-id="3a9e7-166">A Chef Node Run (sorozat) lista.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="3a9e7-167">-Secret</span><span class="sxs-lookup"><span data-stu-id="3a9e7-167">-Secret</span></span>
<span data-ttu-id="3a9e7-168">Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcs.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="3a9e7-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="3a9e7-169">-SecretFile</span></span>
<span data-ttu-id="3a9e7-170">Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcsot tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="3a9e7-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="3a9e7-171">-ValidationClientName</span></span>
<span data-ttu-id="3a9e7-172">Az érvényesítési ügyfél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="3a9e7-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="3a9e7-173">-ValidationPem</span></span>
<span data-ttu-id="3a9e7-174">A Chef validator. PEM fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="3a9e7-175">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3a9e7-175">-Version</span></span>
<span data-ttu-id="3a9e7-176">A séf-kiterjesztés verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="3a9e7-177">-VM</span><span class="sxs-lookup"><span data-stu-id="3a9e7-177">-VM</span></span>
<span data-ttu-id="3a9e7-178">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e7-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="3a9e7-179">-Windows</span></span>
<span data-ttu-id="3a9e7-180">Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.</span><span class="sxs-lookup"><span data-stu-id="3a9e7-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e7-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9e7-181">CommonParameters</span></span>
<span data-ttu-id="3a9e7-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a9e7-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9e7-183">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9e7-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9e7-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a9e7-184">INPUTS</span></span>

## <span data-ttu-id="3a9e7-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a9e7-185">OUTPUTS</span></span>

## <span data-ttu-id="3a9e7-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a9e7-186">NOTES</span></span>

## <span data-ttu-id="3a9e7-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a9e7-187">RELATED LINKS</span></span>

[<span data-ttu-id="3a9e7-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3a9e7-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="3a9e7-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3a9e7-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


